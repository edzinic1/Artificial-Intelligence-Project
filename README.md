# Artificial-Intelligence-project
The project was done by: Šahbaz Emina, Kovačević Nađa and Džinić Edna

# 🧠 Disease Diagnosis Based on Symptoms – AI Project

This project was developed as part of the "Artificial Intelligence" course at the Faculty of Electrical Engineering, University of Sarajevo. The goal is to build an intelligent system that can predict possible diseases based on symptoms provided by the user.

## 📌 Project Description

In modern healthcare, early and accurate diagnosis is essential. This system aims to assist both doctors and patients by providing preliminary disease predictions using machine learning. Users enter symptoms, and the model returns the most probable diagnosis based on previously learned data patterns.
The system uses a supervised learning approach on a medical dataset from Kaggle, mapping symptoms to 41 possible diseases using a multiclass classification model.

## 🧪 Dataset

- **Source**: [Kaggle – Disease Symptom Description Dataset](https://www.kaggle.com/datasets/itachi9604/disease-symptom-description-dataset)
- **Format**: CSV
- **Size**: 4920 instances, 18 attributes (17 symptoms + 1 disease)
- **Classes**: 41 unique diseases
- **Split**: 80% training / 20% testing
- **Additional files**:
  - `Symptom-severity.csv`: symptom weights (1–7)
  - `symptom_Description.csv`: textual disease descriptions
  - `symptom_precaution.csv`: recommended precautions

## ⚙️ Technologies Used

- Python 3
- TensorFlow / Keras
- Pandas, NumPy, Scikit-learn
- Matplotlib for visualizations

## 🧠 Model Architecture

- Input: binary-encoded symptom vector
- **Model**: 3-layer neural network
  - Input layer: 128 neurons, ReLU
  - Hidden layer: 64 neurons, ReLU
  - Output layer: 41 neurons (Softmax)
- **Optimizer**: Adam
- **Loss function**: Categorical Crossentropy
- **Evaluation metric**: Accuracy
- **Training**: 30 epochs, batch size 32

## 📈 Results and Performance

- **Training accuracy**: 99–100% achieved by epoch 2
- **Validation accuracy**: 100%
- **Confusion matrix**: perfect classification on all classes
- **Loss**: almost zero after 3–4 epochs
- **Test results**: No errors, even with custom input testing
- **Note**: Due to unique symptom-disease mapping, the model performs exceptionally well but risks overfitting on non-generalized data

## 💡 Key Features

- Handles missing and inconsistent symptom names
- User can input any combination of symptoms for prediction
- If unknown symptoms are entered, system returns a warning message
- Designed for educational purposes with clear structure and high interpretability
