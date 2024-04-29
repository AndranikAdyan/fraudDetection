# Fraud Detection

This Jupyter Notebook project demonstrates fraud detection using a Decision Tree classifier on financial transaction data. The dataset used (`sp1.csv`) contains the following fields:

- `step`: Time step representing the hour of the transaction.
- `type`: Type of transaction (e.g., CASH_IN, CASH_OUT, DEBIT, PAYMENT, TRANSFER).
- `amount`: Amount of the transaction.
- `nameOrig`: Customer ID of the originator.
- `oldbalanceOrg`: Original balance before the transaction for the originator.
- `newbalanceOrig`: New balance after the transaction for the originator.
- `nameDest`: Customer ID of the recipient.
- `oldbalanceDest`: Original balance before the transaction for the recipient.
- `newbalanceDest`: New balance after the transaction for the recipient.
- `isFraud`: Binary indicator (1 for fraudulent transaction, 0 otherwise).
- `isFlaggedFraud`: Binary indicator (1 if the transaction was flagged as fraudulent based on a certain threshold, 0 otherwise).

The dataset used in this project can be downloaded from [Kaggle](https://www.kaggle.com/datasets/ealaxi/paysim1?resource=download).

## Prerequisites

- Python 3.x
- Jupyter Notebook
- Required Python libraries:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/fraudDetection.git
   ```

2. Navigate to the project directory:
   ```bash
   cd fraudDetection
   ```

3. Install the required Python libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib
   ```

## Usage

1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

2. Open the `fraudDetection.ipynb` notebook in your browser.

3. Run each cell in the notebook sequentially to execute the code blocks.

## Description

- **Dataset**: The dataset (`sp1.csv`) contains financial transaction details including transaction type, amount, originator and recipient details, balances before and after the transaction, and indicators for fraud (`isFraud`) and flagged fraud (`isFlaggedFraud`).

- **Data Preprocessing**:
  - The `type` column is encoded using LabelEncoder to convert text values to integers for modeling purposes.
  - Columns `isFlaggedFraud`, `nameOrig`, `nameDest`, and `isFraud` are dropped from the features (`X`) as well as the target (`Y`).

- **Model Training**:
  - A Decision Tree classifier is used for fraud detection.

- **Evaluation**:
  - The accuracy of the model is evaluated using `accuracy_score`.
  - **Accuracy Score**: The model achieved an accuracy score of 0.99 on the test dataset.

- **Visualization**:
  - A pie chart displays the ratio of fraudulent vs. non-fraudulent transactions in the dataset.
  - A horizontal bar chart shows the number of operations by type.

## File Structure

- `fraudDetection.ipynb`: Jupyter Notebook containing the code for data preprocessing, model training, evaluation, and visualization.
- `datasets/sp1.csv`: Dataset file containing financial transaction data.
