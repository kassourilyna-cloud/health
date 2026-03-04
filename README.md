# Health Risk Prediction Report

## 1. Introduction
This project aims to predict health risk outcomes using **Machine Learning (ML)** and **Deep Learning (DL)** models.  
The goal is to compare different models and assess which performs best on the dataset.

## 2. Methodology
The workflow consists of several steps:

1. **Data Preprocessing**
   - Handling missing values
   - Encoding categorical variables
   - Feature scaling (StandardScaler)
   - Train-test split (cross validation)

2. **Machine Learning Models**
   - Logistic Regression
   - Random Forest
   - Support Vector Machine (optional)

3. **Deep Learning Model**
   - Neural Network with:
     - Input layer
     - 2 Dense layers (ReLU activation)
     - Output layer (Sigmoid for binary classification)
   - Trained with Adam optimizer and Binary Crossentropy loss

4. **Evaluation Metrics**
   - Accuracy, Precision, Recall, F1-score
   - Confusion Matrix

---

## 3. ML Model Results

| Model              | Accuracy | Precision | Recall | F1-score |
|-------------------|---------|-----------|--------|----------|
| Logistic Regression | 0.78    | 0.76      | 0.80   | 0.78     |
| Random Forest       | 0.82    | 0.81      | 0.83   | 0.82     |
| SVM                 | 0.79    | 0.78      | 0.80   | 0.79     |

- **Observations:** Random Forest achieved the highest overall performance.

---

## 4. DL Model Results

- **Architecture:** Input → Dense(64, ReLU) → Dense(32, ReLU) → Output(Sigmoid)  
- **Training:** 50 epochs, batch size = 32  

| Metric        | Value |
|---------------|-------|
| Accuracy      | 0.83  |
| Precision     | 0.82  |
| Recall        | 0.84  |
| F1-score      | 0.83  |

- **Observation:** The DL model slightly outperforms ML models but requires longer training.


## 5. Comparative Analysis
- ML vs DL:
  - ML models are faster to train and interpret.
  - DL gives marginally better accuracy but is less interpretable.
- Feature importance is easier to extract from Random Forest than from DL models.
- Recommendation: Use Random Forest for fast, interpretable results; DL can be used if higher accuracy is critical.

- 
## 6. Conclusion
- Health risk prediction models were successfully developed and evaluated.
- **Random Forest (ML)** provides a good balance of accuracy and interpretability.
- **Deep Learning** slightly improves accuracy but at the cost of complexity.
- Future work: Incorporate more patient data and explore ensemble methods for further performance improvements.
