# ds4002-project3-DataDawgs

## Repository Contents
This repository contains all data, code, and outputs used to build and evaluate a a deep learning model to classify chest X-ray images as normal or abnormal. Using the NIH Chest X-ray dataset, we implement an EfficientNet-based convolutional neural network (CNN) to detect abnormalities and support medical image analysis.

### Folder Structure
- **DATA/**  
  Contains all datasets used in this project.
  
- **OUTPUT/**  
  Contains all generated figures, model outputs, final presentation, and evaluation metrics.

- **SCRIPTS/**  
  Contains the main Jupyter Notebook used for data cleaning, analysis, modeling, and evaluating.

- **LICENSE.md**  
  Describes how this repository can be used and cited.

---

## Software and Platform

### Software Used
- Python 3 (Jupyter Notebook / Google Colab)

### Add-on Packages Used 
- numpy
- pandas
- os
- urllib
- tarfile
- matplotlib
- scikit-learn
- tensorflow

### Platform Used
- macOS / Windows (compatible with both)
- Developed using Jupyter Notebook (can also be run in Google Colab)

---

## Documentation Map

### DATA (folder) contains:
- 'DataAppendix.pdf' (Data Appendix)
- 'Data_Entry_2017_v2020.csv' (CSV file containing X-ray results)

### OUTPUT (folder) contains:
- 'DenseNetConfusionMatrix.png' (Dense Net Confusion Matrix)
- 'DenseNetPredictionDistribution.png' (Dense Net Prediction Distribution Graph)
- 'EfficientNetConfusionMatrix.png' (Efficient Net Confusion Matrix)
- 'EfficientNetPredictionDistribution.png' (Efficient Net Prediction Distribution Graph)
- 'ROCCurveAnalysis.png' (ROC Curve Analysis Graph)

### SCRIPTS (folder) contains:
- 'Project_3_Code.ipynb' (Contains all steps of our code, including pre analysis, analysis, and post analysis)

---

## Instructions for Reproducing Results
1. In GitHub, download the notebook:
   - `Project_3_Code.ipynb`

2. Open **Google Colab** and upload the notebook.

3. (Optional but recommended) Enable GPU:
   - Go to `Runtime` → `Change runtime type`  
   - Select **T4 GPU**  
   - If using Colab Pro, you may select a more powerful GPU (e.g., A100)

4. Run all notebook cells **top-to-bottom**.

---

### The notebook will automatically:

- Download the NIH Chest X-ray image dataset using `urllib`
- Extract and load image files into the runtime environment  
- Load the metadata CSV file (if included in the notebook or repository)

- Clean and preprocess the data:
  - Remove missing or inconsistent entries  
  - Convert labels into binary classes:
    - `No Finding` → **0 (Normal)**  
    - All other labels → **1 (Abnormal)**  

- Preprocess images:
  - Resize to a consistent shape  
  - Normalize pixel values  

- Apply data augmentation:
  - Rotation  
  - Flipping  
  - Scaling  

- Split the dataset into:
  - Training set  
  - Validation set  
  - Test set  

- Load a pretrained **EfficientNet model**
- Modify final layers for binary classification  
- Train the model using transfer learning  

- Evaluate performance using:
  - Accuracy  
  - Precision  
  - Recall (**primary focus**)  
  - F1 Score  
  - Confusion matrix  

---

### Confirm your results by checking:

- Printed evaluation metrics in the notebook output  
- Confusion matrix visualization  
- Model performance meets project benchmark:
  - ~75% accuracy  
  - Strong recall for abnormal cases  

---

### Notes

- The dataset is large and may take several minutes to download and extract  
- Ensure sufficient runtime memory in Colab  
- If the runtime disconnects, you may need to re-run all cells  


---
