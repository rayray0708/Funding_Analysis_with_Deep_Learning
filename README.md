# Funding_Analysis_with_Deep_Learning
Alphabet Soup, a nonprofit foundation, seeks a tool leveraging machine learning and neural networks. My task is to develop a binary classifier using dataset features to predict funding success for applicants, aiding Alphabet Soup in selecting ventures with optimal potential.

## Instructions
* To see the code I generated for the original neural network model, please navigate to `Starter_Code.ipynb`.
* To see the code for the test models and the optimisation process, please navigate to `AlphabetSoupCharity_Optimisation.ipynb`. The optimal model was exported into a H5 file under the name `AlphabetSoupCharity_Optimisation.h5`.
* To see the analysis report I have written, please navigate to `Report` and `Report.md`. 

## Installations
The following dependencies were used to run the code. Please copy the code as is to your code editor:
`from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler, OneHotEncoder
import pandas as pd
import tensorflow as tf
import sklearn as skl
import keras_tuner as kt
from pprint import pprint
from tensorflow.keras.models import load_model, save_model`

Please ensure you have the following libraries pre-installed:
1. `!pip install pandas`
2. `!pip install scikit-learn`
3. `!pip install tensorflow`
4. `!pip install keras-tuner`

## Neural network model analysis
Below is a summary of our dataset:
![Alt text](<Screenshot 2023-12-19 at 1.45.10 pm.png>)

Within this dataset are a number of columns that capture metadata about each organisation, such as:

* `EIN` and `NAME`—Identification columns
* `APPLICATION_TYPE`—Alphabet Soup application type
* `AFFILIATION`—Affiliated sector of industry
* `CLASSIFICATION`—Government organisation classification
* `USE_CASE`—Use case for funding
* `ORGANIZATION`—Organisation type
* `STATUS`—Active status
* `INCOME_AMT`—Income classification
* `SPECIAL_CONSIDERATIONS`—Special considerations for application
* `ASK_AMT`—Funding amount requested
* `IS_SUCCESSFUL`—Was the money used effectively

#### Note that the `EIN` and `NAME` columns have been dropped because they don't contribute to the features of our model.

The pre-processed dataset has the following columns:
![Alt text](<Screenshot 2023-12-19 at 1.51.10 pm.png>)

Finally, our final model has the following features:
![Alt text](<Screenshot 2023-12-19 at 1.53.24 pm.png>)
![Alt text](<Screenshot 2023-12-19 at 1.53.37 pm.png>)

## Contribution
Special thanks to the following individuals for their contribution to the project:
-Camilo Vargas