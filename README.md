

---

# Sebha Breast Cancer Dataset

### Biological & Tumor Marker Dataset for Early Detection

## 📌 Overview

The **Sebha Breast Cancer Prediction Corpus** is a medical dataset collected from the **Sebha Oncology Center (SOC)** in southern Libya. It focuses on using routine blood test data—specifically biological and tumor markers—to predict breast cancer (BC) in its early stages.

This dataset was created to address the lack of breast cancer research in Libya's southern region and to investigate cost-effective alternatives to biopsies for early diagnosis. It serves as a benchmark for evaluating machine learning models, particularly **Classification and Regression Trees (CART)**, in medical diagnostics.

## 📊 Dataset Statistics

| Attribute | Value |
| --- | --- |
| **Total Cases** | **2,435** |
| **Time Period** | 2015 – 2020 |
| **Source** | Sebha Oncology Center (SOC) routine blood tests |
| **Class Distribution** | Benign (55.9%), Malignant (44.1%) |
| **Features** | 23 clinical attributes (Biological & Tumor Markers) |
| **Target Variable** | Diagnosis (0 = Benign, 1 = Malignant) |

---

## 📁 Data Features

The dataset contains **23 features** categorized into patient demographics, biological markers (BM), and tumor markers (TM).

### Key Predictors (Top Correlated Features)

Based on correlation analysis, these features have the strongest relationship with the diagnosis:

* **`CA-15.3`**: Cancer Antigen 15-3 (Strongest positive correlation)
* **`CEA`**: Carcinoembryonic Antigen
* **`LDH`**: Lactate Dehydrogenase
* **`PLT`**: Platelets Count
* **`WBC`**: White Blood Cells Count
* **`ALB`**: Albumin

### Full Feature List

| Category | Features |
| --- | --- |
| **Demographics** | `Age`, `Sex`, `Address` |
| **Tumor Markers** | `CA-15.3`, `CEA` |
| **Blood Counts** | `WBC` (White Blood Cells), `RBC` (Red Blood Cells), `HGB` (Hemoglobin), `PLT` (Platelets) |
| **Kidney Function** | `Urea`, `Creatinine`, `Na+` (Sodium), `K` (Potassium), `CL-` (Chloride) |
| **Liver Function** | `GPT`, `GOT`, `ALP` (Alkaline Phosphatase), `ALB` (Albumin) |
| **Metabolic/Other** | `FBS` (Blood Glucose), `T.Ca` (Total Calcium), `ESR` (Erythrocyte Sedimentation Rate), `LDH` |

---

## 🧹 Preprocessing Pipeline

To prepare the clinical data for machine learning, the following steps were taken:

* **Outlier Handling:** Z-score normalization was applied to sensitive features (`FBS`, `ALP`, `CA15.3`, `RBC`, `PLT`, `LDH`, `K`) to reduce the impact of extreme values.
* **Feature Selection:** Strongest predictors were identified via correlation coefficient analysis.
* **Data Splitting:** 80% Training, 20% Testing.
* **Cross-Validation:** 5-Fold Cross-Validation was determined to be the optimal splitting strategy.

---

## 🧪 Benchmark Results

The dataset was used to train and optimize a **Classification and Regression Tree (CART)** model, which was compared against other classical algorithms. The optimized CART model achieved the best performance.

| Model | Accuracy | Precision | Recall | F1-Score |
| --- | --- | --- | --- | --- |
| **Optimized CART** | **66%** | **0.65** | **0.67** | **0.67** |
| Original CART | 63% | 0.63 | 0.63 | 0.63 |
| Logistic Regression (LG) | 60% | - | - | - |
| Naïve Bayes (NB) | 58% | - | - | - |
| K-Nearest Neighbors (KNN) | 57% | - | - | - |

*Note: The optimized CART model also achieved the lowest error rates (MAE: 0.32, RMSE: 0.57) and the highest Area Under Curve (AUC) score of 0.64.*

---

## 📚 Citation

If you use this dataset, please cite the original paper:

```bibtex
@INPROCEEDINGS{9837543,
  author={Agaal, Asma and Essgaer, Mansour},
  booktitle={2022 IEEE 2nd International Maghreb Meeting of the Conference on Sciences and Techniques of Automatic Control and Computer Engineering (MI-STA)}, 
  title={Biological and Tumor Markers in Early Prediction Phase of Breast Cancer Using Classification and Regression Tree: Sebha Oncology Center as a Case study}, 
  year={2022},
  volume={},
  number={},
  pages={228-233},
  keywords={White blood cells;Red blood cells;Conferences;Medical services;Oncology;Prediction algorithms;Breast cancer;breast cancer;biological markers;tumor markers;classification algorithm;routine blood test;Sebha oncology center;Libya},
  doi={10.1109/MI-STA54861.2022.9837543}}


```

---

## 📄 License

This data is associated with the research presented in the paper. Please refer to the original authors or the Sebha Oncology Center for specific usage rights and licensing information.
