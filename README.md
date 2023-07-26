# Fake-News-Detector
### A Fake News Prediction System using Machine Learning with Python.
- Algorithm: Logistic Regression model for prediction

## Importing Kaggle Dataset into Jupyter

To import a dataset from Kaggle into Jupyter Notebook, you'll need to follow these steps:

- Create a Kaggle Account and API Token:

>> If you don't have a Kaggle account, create one on the Kaggle website.
Go to your Kaggle account, click on "My Account," scroll down to the "API" section, and click "Create New API Token." This will download a file named kaggle.json, which contains your API credentials.
Install Kaggle Library:

In Jupyter Notebook, you'll need to install the Kaggle library. You can do this by running the following command in a code cell:
diff
Copy code
!pip install kaggle
Upload Kaggle API Token:

Upload the kaggle.json file you downloaded earlier into the same directory where your Jupyter Notebook is located. This will allow the Kaggle library to access your Kaggle account.
Import the Dataset:

In your Jupyter Notebook, you can now use the Kaggle library to directly download datasets from Kaggle. Use the kaggle datasets download command along with the dataset's URL or dataset ID to download it. For example:
python
Copy code
!kaggle datasets download -d username/dataset-name
Unzip the Dataset:

The downloaded dataset will be in a compressed format (e.g., zip). You can use the unzip command to extract its contents. For example:
python
Copy code
!unzip dataset-name.zip
Read the Dataset into a DataFrame:

After extracting the dataset, you can use Pandas to read the data into a DataFrame and start exploring and analyzing it. For example:
python
Copy code
import pandas as pd

df = pd.read_csv('dataset-name.csv')  # Adjust the filename and format as per your dataset
Data Analysis and Usage:

Now that you have the dataset loaded into a DataFrame, you can perform various data analysis tasks, data cleaning, visualization, machine learning, etc., depending on your project's requirements.
Remember that you need to replace username/dataset-name with the appropriate Kaggle username and dataset name you want to download. Also, ensure that you have the necessary permissions to access the dataset on Kaggle. If the dataset is private, you might need to use additional commands to authenticate your API token.
