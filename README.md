# Diabetes Prediction Using Feedforward Neural Network

## Overview

This project predicts diabetes outcomes using a feedforward neural network implemented in PyTorch and trained on the Pima Indians Diabetes dataset. It covers preprocessing, training, evaluation, model deployment, and interactive prediction via Gradio.

***

## Key Features

- **Data Preprocessing:** Handles missing values, standardizes features.
- **Model Design:** Feedforward neural network with three fully connected layers.
- **Training & Evaluation:** Includes accuracy, confusion matrix, classification report, and ROC curve.
- **Interactive Demo:** Gradio interface for live diabetes risk prediction.
- **Model Checkpoint:** Saves and loads trained models for inference.

***

## Project Steps

1. **Setup and Requirements**
   - Install required packages:
     ```bash
     pip install -r requirements.txt
     ```

2. **Data Processing**
   - Loads and cleans `diabetes.csv`.
   - Standardizes features using `StandardScaler`.
   - Splits data into training and test sets (80/20).

3. **Model Training**
   - Defines a neural network with input size 8 (features).
   - Trains for 50 epochs using Adam optimizer and BCEWithLogitsLoss.
   - Tracks loss per epoch.

4. **Evaluation & Visualization**
   - Computes accuracy (~72%).
   - Shows confusion matrix and classification report.
   - Plots ROC curve and AUC.

5. **Model Saving & Loading**
   - Saves model and scaler as `diabetesmodelwithscaler.pth`.
   - Demonstrates loading for later inference.

6. **Interactive Gradio Demo**
   - Predicts diabetes by entering patient features.
   - Displays probability and diabetic/not diabetic result.

***

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Hassansyed21/diabetes-prediction-feedforward-nn.git
   cd diabetes-prediction-feedforward-nn
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Notebook**
   - Open `diabetes-model-prediction.ipynb` in Jupyter or Colab.
   - Follow code cells for training and evaluation.

4. **Launch Gradio Demo**
   - Run Gradio cell to launch interactive app:
     ```python
     iface.launch(debug=True)
     ```

***

## File Structure

```
/diabetes-prediction-feedforward-nn
  |-- README.md
  |-- diabetes.csv
  |-- diabetes-model-prediction.ipynb
  |-- diabetes-model-prediction.pdf
  |-- diabetesmodelwithscaler.pth
  |-- requirements.txt
  |-- LICENSE
  |-- assets/
      |-- confusion-matrix.png
      |-- roc-curve.png
```

***

## Results

- **Test Accuracy:** ~72%
- **Confusion Matrix:** Visualizes prediction results.
- **Classification Report:** Shows precision, recall, F1-score.
- **ROC Curve & AUC:** Demonstrates model performance.

***

## Usage Example

Simply enter patient details:
- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age

Get live predictions of diabetes risk via Gradio.

***

## Extending the Project

- Integrate new datasets for broader validation.
- Explore additional neural architectures or machine learning models.
- Deploy via FastAPI or Streamlit for advanced serving.
- Integrate database backends (e.g., MySQL) for scalable data handling.

***

## License

MIT
