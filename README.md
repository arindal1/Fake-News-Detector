# Fake News Detector using Logistic Regression

![Fake News Detector](resources/scs1.png)

Welcome to the **Fake News Detector using Logistic Regression** repository! This repository contains the code implementation of a fake news detector using a logistic regression model. The project aims to identify and classify news articles as either real or fake based on their content.

## Overview

Fake news has become a concerning issue in today's information-driven world. The **Fake News Detector** project addresses this problem by leveraging machine learning techniques to classify news articles as genuine or fabricated. This repository provides a detailed implementation of the solution, from data preprocessing to model training and testing.

![Fake News Detector](resources/scs2.png)

## Features

- Logistic Regression Model: The core of the project uses a logistic regression model to classify news articles.
- Text Preprocessing: The project demonstrates text preprocessing techniques such as stemming and TF-IDF vectorization.
- Dataset: The dataset used for training and testing the model is downloaded from Kaggle's "Fake News" competition.
- Jupyter Notebook: The project code is provided as a Jupyter Notebook for easy understanding and execution.

## Installation and Usage

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/arindal1/Fake-News-Detector.git
   cd Fake-News-Detector
   ```

2. Open the Jupyter Notebook in your preferred environment:

   ```bash
   jupyter notebook Fake_News_Detector.ipynb
   ```

3. Follow the step-by-step instructions in the Jupyter Notebook to explore, execute, and understand the project code.

## Dataset

The dataset used in this project is downloaded from Kaggle's ["Fake News"](https://www.kaggle.com/competitions/fake-news) competition. It consists of news articles labeled as either real or fake.

![Fake News Detector](resources/scs3.png)

## Dependencies

The project requires the following libraries and dependencies:

- NumPy
- Pandas
- scikit-learn
- nltk
- Jupyter Notebook

Ensure that you have these dependencies installed in your environment before running the notebook.

## How does it work?

The provided code implements a fake news detector using a logistic regression model. It involves several steps, such as importing datasets, pre-processing data, stemming, vectorization, splitting data, training the model, and making predictions. I'll explain each section of the code in detail:

### Step 1: Importing Libraries and Datasets

The initial code block imports necessary libraries and downloads the dataset directly from Kaggle. It installs the Kaggle API library (`!pip install kaggle`), downloads the dataset (`!kaggle competitions download -c fake-news`), and unzips it (`!unzip fake-news.zip`).

![Fake News Detector](resources/scs4.png)

### Step 2: Data Preprocessing

#### Stopwords

Stopwords are common words that don't provide significant meaning in natural language text. The code attempts to download the stopwords list from the NLTK library. However, it seems to encounter a connection issue (`[nltk_data] Error loading stopwords: <urlopen error [WinError 10061] No connection could be made because the target machine actively refused it>`), which might require an internet connection to resolve.

### Step 3: Pre-Processing the Data

1. The dataset is imported into a Pandas DataFrame named `news_dataset`.
2. Missing values in the dataset are handled by filling them with empty strings.
3. The 'content' column is created by merging the 'author' name and 'title' of each news article.
4. The data and labels are separated into `X` and `Y` respectively.

### Step 4: Stemming Process

The code uses stemming to reduce words to their root form. A stemming function is defined, which:
1. Removes non-alphabet characters and converts to lowercase.
2. Tokenizes the text into words.
3. Applies stemming to each word and removes stopwords.
4. Joins the stemmed words back into a sentence.

The `apply` method is used to apply this stemming function to the 'content' column of the DataFrame.

### Step 5: Converting to Numerical Data (TF-IDF Vectorization)

The text data is transformed into numerical format using Term Frequency-Inverse Document Frequency (TF-IDF) vectorization. The `TfidfVectorizer` from Scikit-Learn is used to tokenize, build a vocabulary, and calculate the TF-IDF scores for each word in the 'content' column. The transformed data is stored in the variable `X`.

### Step 6: Splitting Training and Testing Data

The data is split into training and testing sets using the `train_test_split` function from Scikit-Learn. The testing set constitutes 20% of the data, and stratification is applied based on the 'label' column to ensure similar class distribution in both sets.

### Step 7: Training the Model

A logistic regression model is initialized using `LogisticRegression()` and trained using the training data (`X_train`, `Y_train`) using the `fit` method.

### Step 8: Model Accuracy

1. The accuracy of the model on the training data is calculated by predicting the labels using the training data and comparing with the actual labels. The accuracy score is printed.
2. Similarly, the accuracy of the model on the testing data is calculated and printed.

### Step 9: Prediction

1. An example instance (`X_new`) from the testing data is selected.
2. The trained model is used to predict whether the news is fake or real.
3. The prediction result is printed based on the predicted label (0 for real, 1 for fake).
4. The actual label is retrieved from the testing data (`Y_test[3]`) and compared to the prediction result to confirm correctness.

Overall, this code demonstrates the process of building a fake news detector using a logistic regression model, including data preprocessing, stemming, TF-IDF vectorization, model training, and predictions.

## Contributing

Contributions to this repository are welcome! If you find any issues, have suggestions, or want to improve the code, feel free to submit a pull request.

## Contact

If you have any questions or want to connect, feel free to reach out:

- GitHub: [arindal1](https://github.com/arindal1)
- LinkedIn: [Arindal](https://www.linkedin.com/in/arindalchar/)
- kaggle: [arindal](https://www.kaggle.com/arindal)
- Dataset Link: <a href="https://www.kaggle.com/competitions/fake-news/data" target="_blank"> Kaggle </a>
- Google Collab Link: <a href="https://colab.research.google.com/drive/1YxD2SRlRn9YfG5Lak7Pr9b8Y7bg6maOZ?authuser=0#scrollTo=HZtk5pq2T8Ey" target="_blank"> Collab </a>

### Happy detecting and learning! 🕵️‍♂️
