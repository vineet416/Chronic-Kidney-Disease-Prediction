# Chronic Kidney Disease Prediction
 
A machine-learning project that predicts whether a patient has chronic kidney disease (CKD) from 24 clinical and lab measurements. It covers exploratory analysis, preprocessing, and a comparison of eight tuned classifiers. The goal is a fast, data-driven screening aid for early CKD detection.

## Project Files

| File | Description |
|---|---|
| `kidney_disease.csv` | Raw dataset: 400 patients, 26 columns (incl. `id`) |
| `EDA_and_Preprocessing.ipynb` | Cleaning, EDA, imputation, encoding, VIF feature selection, split, scaling |
| `Model_Training_and_Evaluation.ipynb` | Trains 8 baseline models, tunes each, compares test accuracy |
| `preprocessed_dataset/` | `X_train`, `X_test`, `y_train`, `y_test` CSVs (320 / 80 rows, 16 features) |

## Dataset

400 patients, 24 features plus target `classification` (`ckd` = 250, `notckd` = 150).

| Group | Columns |
|---|---|
| Demographics / vitals | `age`, `bp` (blood pressure) |
| Urine tests | `sg` (specific gravity), `al` (albumin), `su` (sugar), `rbc`, `pc` (pus cell), `pcc` (pus cell clumps), `ba` (bacteria) |
| Blood chemistry | `bgr` (glucose), `bu` (urea), `sc` (creatinine), `sod`, `pot`, `hemo`, `pcv`, `wc`, `rc` |
| History / symptoms | `htn`, `dm`, `cad`, `appet`, `pe` (pedal edema), `ane` (anaemia) |

## Approach

1. **Understand data** – shape, dtypes, missing values, category values.
2. **Clean** – drop `id`; convert `pcv`, `wc`, `rc` to numeric; fix stray tabs/spaces in `dm`, `cad`, `classification`.
3. **Explore** – univariate, bivariate and multivariate plots (matplotlib, seaborn, plotly).
4. **Prepare** – median imputation (numeric), mode imputation (categorical), label encoding, `ckd`=0 / `notckd`=1.
5. **Select features** – iterative VIF pruning drops 8 columns, leaving 16 features.
6. **Split and scale** – 80/20 split (`random_state=1`), `StandardScaler` fitted on train.
7. **Model** – 8 classifiers, tuned with GridSearchCV / RandomizedSearchCV (5-fold CV).

## Results

Accuracy on the 80-row test set (47 CKD, 33 not CKD):

| Model | Baseline | Tuned | CKD cases missed |
|---|---|---|---|
| SVM | 0.9125 | **0.975** | 2 |
| Random Forest | 0.9625 | **0.975** | 2 |
| AdaBoost | 0.9625 | **0.975** | 2 |
| XGBoost | 0.9875 | **0.975** | 2 |
| Logistic Regression | 0.900 | 0.9625 | 3 |
| Naive Bayes | 0.950 | 0.950 | 4 |
| Gradient Boosting | 0.9625 | 0.950 | 3 |
| Decision Tree | 0.9375 | 0.9375 | 4 |

## Key Insights

- **Classes are imbalanced**: 62.5% CKD vs 37.5% not CKD.
- **Every binary flag separates cleanly**: 0 of 146–149 non-CKD patients show hypertension, diabetes, CAD, pedal edema, anaemia, poor appetite, pus cell clumps or bacteria. Among CKD patients: hypertension 58.8%, diabetes 54.8%, poor appetite 32.8%, pedal edema 30.4%.
- **Kidney markers differ sharply** (median, CKD vs not CKD): creatinine 2.25 vs 0.90, urea 53 vs 33, haemoglobin 10.9 vs 15.0, packed cell volume 33 vs 46.
- **Albumin in urine**: 62% of CKD patients have albumin > 0; no non-CKD patient does.
- **Four models tie at 97.5%** (78/80 correct); they miss 2 CKD patients each and raise no false alarms.
- **Missingness differs by class**: 82.8% of CKD rows have at least one missing value vs 23.3% of non-CKD rows.

## Tech Stack

Python 3.12 · pandas · NumPy · matplotlib · seaborn · plotly · scikit-learn (LabelEncoder, StandardScaler, GridSearchCV, RandomizedSearchCV) · statsmodels (VIF) · XGBoost · Jupyter

## How to Use

1. Clone: `git clone https://github.com/vineet416/Chronic-Kidney-Disease-Prediction.git`
2. Install packages: `pip install pandas numpy matplotlib seaborn plotly scikit-learn statsmodels xgboost jupyter` (no `requirements.txt` is provided).
3. Run `EDA_and_Preprocessing.ipynb` from the repo root; it writes the four CSVs to the working directory.
4. Run `Model_Training_and_Evaluation.ipynb`. It reads `X_train.csv` etc. from its own folder, so copy them out of `preprocessed_dataset/` or change the paths.
