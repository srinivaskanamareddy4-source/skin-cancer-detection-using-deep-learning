# Skin Cancer Detection Using Deep Learning

## Project Overview
This project presents a deep learning-based approach for skin lesion segmentation and classification by combining dermoscopic images with clinical features.

The system uses U-Net for lesion segmentation, EfficientNetB0 for image feature extraction, an autoencoder-based feature fusion approach, and Grad-CAM for model explainability.

## Objectives
- Detect and analyze skin lesions from dermoscopic images.
- Segment lesion regions using U-Net.
- Extract image and clinical features.
- Combine features using an autoencoder-based fusion model.
- Classify skin lesions into seven categories.
- Visualize model predictions using Grad-CAM.

## Methodology

1. **Data Collection:** HAM10000 dataset with clinical metadata and ISBI2016 image-mask data.
2. **Preprocessing:** Image resizing, hair removal, normalization, and data augmentation.
3. **Segmentation:** U-Net model for skin lesion segmentation.
4. **ROI Extraction:** Extracting the region of interest using predicted segmentation masks.
5. **Feature Extraction:** EfficientNetB0 image features and clinical features such as age, sex, and localization.
6. **Feature Fusion:** Autoencoder bottleneck to combine image and clinical features.
7. **Classification:** EfficientNetB0-based deep learning classification model.
8. **Explainability:** Grad-CAM visualization to understand model predictions.

## Technologies Used
- Python
- TensorFlow / Keras
- CNN
- EfficientNetB0
- U-Net
- OpenCV
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Google Colab

## Dataset
- HAM10000: Dermoscopic images and clinical metadata.
- ISBI2016: Images and segmentation masks used to train the U-Net model.

Note: The datasets are not included in this repository. The notebook uses Google Drive dataset paths, so dataset folders and paths must be configured before execution.

## Classification Categories
The model classifies skin lesions into seven categories:

- AKIEC
- BCC
- BKL
- DF
- MEL
- NV
- VASC

## Model Performance

| Evaluation Metric | Result |
|---|---:|
| Test Accuracy | 72.65% |
| Balanced Accuracy | 66.20% |
| Macro F1 Score | 57.88% |
| Macro AUC (8-view TTA) | 93.19% |
| U-Net Validation Dice Score | 89.13% |

The evaluation uses a held-out test set of 1,481 images. The data split is grouped by lesion ID to avoid the same lesion appearing across training, validation, and test sets.

## Repository Contents
- `Skin_Cancer_Methodology_Pipeline.ipynb` – Complete project implementation.
- `README.md` – Project documentation.
- `.gitignore` – Git ignored files configuration.

## How to Run
1. Open the notebook using Google Colab.
2. Download or obtain the required HAM10000 and ISBI2016 datasets.
3. Upload the datasets to Google Drive.
4. Update the dataset paths in the notebook.
5. Install the required Python libraries.
6. Run the notebook cells in order.

## Future Improvements
- Improve classification performance, especially for underrepresented classes.
- Explore additional deep learning architectures.
- Improve clinical feature integration.
- Develop a user-friendly web application.

## Disclaimer
This project is an academic research prototype for educational purposes only. It is not a clinically validated diagnostic system and must not be used as a substitute for professional medical advice.

## Author
Srinivas Kanamareddy

Electronics and Communication Engineering Undergraduate
