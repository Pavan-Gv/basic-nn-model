# Developing a Neural Network Regression Model

## AIM

To develop a neural network regression model for the given dataset.

## THEORY

Explain the problem statement

## Neural Network Model

Include the neural network model diagram.

## DESIGN STEPS

### STEP 1:

Loading the dataset

### STEP 2:

Split the dataset into training and testing

### STEP 3:

Create MinMaxScalar objects ,fit the model and transform the data.

### STEP 4:

Build the Neural Network Model and compile the model.

### STEP 5:

Train the model with the training data.

### STEP 6:

Plot the performance plot

### STEP 7:

Evaluate the model with the testing data.

## PROGRAM:
```
Developed By: G Venkata Pavan Kumar
RegNo: 212221240013
```

```
from google.colab import auth
import gspread
from google.auth import default
import pandas as pd

auth.authenticate_user()
creds, _ = default()
gc = gspread.authorize(creds)

worksheet = gc.open('StudentsData').sheet1

rows = worksheet.get_all_values()

df = pd.DataFrame(rows[1:], columns=rows[0])
df = df.astype({'Input':'float'})
df = df.astype({'Output':'float'})
df.head()

```
## Dataset Information

<img width="138" alt="image" src="https://github.com/Pavan-Gv/basic-nn-model/assets/94827772/21d61956-2559-465a-8c8b-ac0f1d11e652">

## OUTPUT:

### Training Loss Vs Iteration Plot

<img width="327" alt="image" src="https://github.com/Pavan-Gv/basic-nn-model/assets/94827772/d2cf233c-906c-4cd3-a0bf-0b6569a3898d">

### Test Data Root Mean Squared Error

<img width="326" alt="image" src="https://github.com/Pavan-Gv/basic-nn-model/assets/94827772/1b1d5640-5dc8-4c5a-b378-19888609f810">


### New Sample Data Prediction

<img width="233" alt="image" src="https://github.com/Pavan-Gv/basic-nn-model/assets/94827772/7e72c01d-7ba7-4b2d-b4f4-8409f115b730">

## RESULT:
Therefore We successfully developed a neural network regression model for the given dataset.
