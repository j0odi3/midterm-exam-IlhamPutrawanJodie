# midterm-exam-IlhamPutrawanJodie
# ATS Machine Vision — HOG + SVM Digit Recognition

Overview  
This project implements a **machine vision system** for handwritten digit recognition using:
- **Histogram of Oriented Gradients (HOG)** for feature extraction  
- **Support Vector Machine (SVM)** for classification  

The dataset used is **EMNIST (Extended MNIST)**, which contains thousands of handwritten digits and letters in CSV format.

---

## ⚙️ Features
1. **Data Loading**  
   - Loads EMNIST datasets for training and testing (`emnist-digits-train.csv`, `emnist-digits-test.csv`).
   - Each image (28×28 pixels) is reshaped and normalized.

2. **Feature Extraction (HOG)**  
   - Extracts image features using **Histogram of Oriented Gradients**.  
   - Captures edge and shape information for better digit distinction.

3. **Model Training (SVM)**  
   - Trains an **SVM classifier** on extracted HOG features.  
   - Finds the optimal hyperplane to separate digits.

4. **Model Evaluation**  
   - Tests model performance using unseen test data.  
   - Evaluates using:
     - Accuracy score  
     - Confusion Matrix  
     - LOOCV (Leave-One-Out Cross Validation)

5. **Output Files**
   - `model_hog_svm.pkl` — trained SVM model  
   - `model_hog_svm_loocv.pkl` — LOOCV-trained model  
   - `confusion_matrix_hog_svm.png` — confusion matrix visualization  
   - `log.txt` — training log file  
   - `loocv_scores.csv` — LOOCV accuracy results  
   - `output/` — directory for additional results

---

Results
| Metric | Description | Result |
|--------|--------------|--------|
| Accuracy | Overall digit recognition accuracy | **~95–97%** |
| Validation | Leave-One-Out Cross Validation | ✅ Stable results |
| Dataset | EMNIST Digits |  |

**Confusion Matrix:**  
The confusion matrix (`confusion_matrix_hog_svm.png`) shows strong diagonal dominance, meaning most digits are correctly classified with few misclassifications.

---

Summary
This project demonstrates how **HOG features combined with SVM** can effectively recognize handwritten digits with high accuracy and reliability.  
The implementation can be extended to various **machine vision** applications, such as:
- License plate recognition  
- Industrial inspection  
- Robotic vision and automation  

