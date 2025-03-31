# Chronic Kidney Disease Prediction

This repository contains the code for the Chronic Kidney Disease Detection Prediction Project. The goal of this project is to predict chronic kidney disease using various health parameters such as Diabetes Mellitus, Blood Urea, Sugar, Hypertension, etc.

## Table of Contents

- [Project Description](#project-description)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Models and Algorithms](#models-and-algorithms)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)
- [Contact](#contact)

## Project Description

Chronic Kidney Disease (CKD) is a significant public health issue affecting millions of individuals worldwide. Early detection and treatment of CKD can prevent the progression to kidney failure. This project leverages various machine learning algorithms to predict the likelihood of CKD based on multiple health parameters. The model with the highest accuracy score of 97.5% has been achieved through hyperparameter tuning.

## Features

- Predicts the likelihood of chronic kidney disease
- Utilizes multiple machine learning algorithms
- Hyperparameter tuning for optimizing model performance
- Achieves an accuracy score of 97.5%

## Dataset

The dataset used for this project includes various health parameters such as:

- Age
- Blood Pressure
- Specific Gravity
- Albumin
- Sugar
- Red Blood Cells
- Pus Cell
- Pus Cell Clumps
- Bacteria
- Blood Glucose Random
- Blood Urea
- Serum Creatinine
- Sodium
- Potassium
- Hemoglobin
- Packed Cell Volume
- White Blood Cell Count
- Red Blood Cell Count
- Hypertension
- Diabetes Mellitus
- Coronary Artery Disease
- Appetite
- Pedal Edema
- Anemia

## Installation

To run this project locally, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/vineet416/Chronic-Kidney-Disease-Prediction.git
    ```

2. Navigate to the project directory:
    ```bash
    cd Chronic-Kidney-Disease-Prediction
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

To use the model for prediction, follow these steps:

1. Open the Jupyter Notebook:
    ```bash
    jupyter notebook
    ```

2. Open the `Chronic_Kidney_Disease_Prediction.ipynb` file.

3. Follow the instructions in the notebook to load the dataset, train the model, and make predictions.

## Models and Algorithms

The following machine learning algorithms were used in this project:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- XGBoost

Hyperparameter tuning was performed to optimize each model's performance. The Random Forest Classifier achieved the highest accuracy score of 97.5%.

## Results

The performance of each model was evaluated using accuracy, precision, recall, and F1-score. The Random Forest Classifier outperformed other models with an accuracy score of 97.5%. Below are the results for each model:

| Model                  | Accuracy | Precision | Recall | F1-Score |
|------------------------|----------|-----------|--------|----------|
| Logistic Regression    | 94.5%    | 92.3%     | 95.1%  | 93.7%    |
| Decision Tree          | 96.0%    | 94.8%     | 96.5%  | 95.6%    |
| Random Forest          | 97.5%    | 96.8%     | 97.9%  | 97.3%    |
| Support Vector Machine | 95.2%    | 93.5%     | 95.7%  | 94.6%    |
| K-Nearest Neighbors    | 93.8%    | 91.2%     | 94.3%  | 92.7%    |
| XGBoost                | 96.8%    | 95.4%     | 97.1%  | 96.2%    |

## Contributing

If you would like to contribute to this project, please follow these steps:

1. Fork the repository.

2. Create a new branch:
    ```bash
    git checkout -b feature/YourFeatureName
    ```

3. Make your changes and commit them:
    ```bash
    git commit -m 'Add some feature'
    ```

4. Push to the branch:
    ```bash
    git push origin feature/YourFeatureName
    ```

5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgments

- Special thanks to the contributors and the community for their support.
- Thanks to the providers of the dataset used in this project.

## Contact

For any questions or inquiries, please contact [Vineet](https://github.com/vineet416).
