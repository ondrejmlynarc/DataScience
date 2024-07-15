# Car Purchase Prediction using Artificial Neural Networks (ANNs)

## Overview
This project aims to develop a predictive model using ANNs to forecast the total dollar amount customers are likely to spend on car purchases. The model leverages various customer attributes, including gender, age, annual salary, credit card debt, and net worth.

## Dataset
The model is trained on the Kaggle 'Car_Purchasing_Data.csv' dataset, which contains information on 500 customers. The relevant attributes used for prediction are:

- **Gender**
- **Age**
- **Annual Salary**
- **Credit Card Debt**
- **Net Worth**

The target variable is the 'Car Purchase Amount,' representing the total dollar value customers are expected to spend on their car purchase.

## Methodology

### Data Loading and Preprocessing:

1. Load the 'Car_Purchasing_Data.csv' dataset using pandas.
2. Remove irrelevant columns ('Customer Name,' 'Customer e-mail,' 'Country').
3. Scale the features between 0 and 1 using MinMaxScaler.
4. Split the data into training (75%) and testing (25%) sets.

### Model Building:

Build a Sequential model with:
- Input layer with 5 neurons (representing the 5 features).
- Two hidden layers with 25 neurons each, using ReLU activation.
- Output layer with 1 neuron (representing the predicted 'Car Purchase Amount'), using linear activation.
- Compile the model with the Adam optimizer and mean squared error loss.

### Model Training:

- Train the model for 20 epochs with a batch size of 25.
- Monitor the training and validation loss during training.

### Model Evaluation:

- Predict the 'Car Purchase Amount' on the test set.
- Evaluate the model's performance using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared (R2).

## Results
The model demonstrates reasonable performance, with relatively low MSE and MAE values and a high R-squared value. This indicates that it captures a significant portion of the variance in the target variable and can provide accurate predictions.

## Example Usage
To predict the expected purchase amount for a customer with the following attributes:
- **Gender**: Male (1)
- **Age**: 50 years old
- **Annual Salary**: $50,000
- **Credit Card Debt**: $10,985
- **Net Worth**: $629,312

The model predicts an expected purchase amount of approximately $168,877.

## Conclusion
The developed ANN model offers a valuable tool for car salesmen to predict car purchase amounts based on customer attributes. By utilizing this model, businesses can gain insights into customer preferences, personalize interactions, and ultimately improve sales outcomes.

## Future Work
Potential areas for further improvement include:
- Experimenting with different model architectures and hyperparameters.
- Incorporating additional customer attributes or external factors.
- Validating the model on a larger, more diverse dataset.
- Deploying the model as a user-friendly application for real-world use.
