
# Potato Disease Detection using KNN
The analysis of potato leaf is done by extracting its color and texture feature and classification/detection of disease is done using KNN classifier. 

## About Dataset
The dataset used for this project has been taken from well known __Plant-Village Dataset__. Images on Poatao leaves are categorize as early blight, late blight and healthy leaves.

## Steps Involved
The step-by-step procedure of the proposed system is: 
- Image Acquisition
- Image Enhancement
- Feature Extraction (Color and Texture Feature Extraction)
- Classification

**Image Acquisition:** In the initial step, the RGB images of potato leaf samples were taken.

**Image Enhancement:** Then resizing of image into 32X32 dimension is done. The resized RGB image is then Converted to HSV image and GRAY image. The HSV image is then masked to segment the disease portion of the leaf. Bitwise_and masking is used for segmentation

**Feature Extraction:** Feature extraction includes color feature extraction and texture feature extraction.

**Color Feature Extraction:** While color features are extracted, HSV image is taken and HSV value is extracted which is flattened for Euclidean distance calculation within origin. Then the sum value is calculated.

**Texture Feature Extraction:** While the texture feature is extracted, a GRAY image is taken and the GLCM (Gray Level Co-occurrence Method) is created using greycomatrix. After that, several properties are extracted from GLCM (Gray Level Co-occurrence Method) using greycoprops. These properties provide information about the texture of the image. The properties extracted are 'contrast', 'correlation', 'dissimilarity', 'homogeneity', 'ASM' and 'energy'.


**Classification:** From the previous results KNN classifier is used to detect the potato leaf disease.
