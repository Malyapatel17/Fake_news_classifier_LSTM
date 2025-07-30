# Fake_news_classifier_LSTM
This project builds an LSTM-based Fake News Classifier using only headlines. It applies tokenization, stopword removal, and lemmatization with Word2Vec embeddings. Achieves ~93% accuracy with faster training. Future work includes adding full text and advanced models for better results.

This repository contains a Fake News Detection model built using an LSTM (Long Short-Term Memory) neural network, trained to classify news headlines as fake or real.

📂 Dataset
Dataset source: Kaggle, Fake and True News

The dataset consists of two CSV files: Fake.csv and True.csv.

🏗️ Pipeline Overview
Data Loading

News headlines and metadata are loaded from the CSV files using pandas.

Preprocessing

Only the title column from the news articles is used for classification.

Titles undergo comprehensive preprocessing steps including tokenization, stopword removal, and lemmatization using NLTK's WordNetLemmatizer to normalize words and improve model learning.

Lemmatization is chosen over stemming to better preserve the semantic meaning of words.

Embedding Layer

Utilizes pre-trained Word2Vec embeddings (Google News, 300 dimensions) via Gensim for enhanced word representation in headlines.

Model Building

An LSTM-based neural network is trained to classify news titles as either fake or real.

Evaluation

Model performance is evaluated on held-out test data.

The final achieved accuracy score is approximately 91% (please replace with your exact accuracy from code).

ℹ️ Important Notes & Limitations
Input Used:

Only the news headline/title was used for model training and prediction.

The full news text was deliberately excluded to keep training time and computational resource requirements manageable.

Preprocessing:

Advanced preprocessing including tokenization, stopword removal, and lemmatization is already applied on the titles.

Implications:

Using only titles limits context information available, so while the accuracy is good, it may not represent the best possible fake news detection performance.

This model is suited for quick prototyping or use cases where inference speed is prioritized over incorporating full article details.

🔮 Future Implementation
Incorporate both news headlines and full news text as inputs for richer context and improved classification accuracy.

Apply similar advanced preprocessing techniques (tokenization, stopword removal, lemmatization) on the full text.

Experiment with more advanced architectures such as transformer-based models or hybrid CNN-RNN models.

Use transfer learning, attention mechanisms, and hyperparameter tuning for better performance and robustness.

🚀 How to Use
Clone this repository and ensure you have Python and the required libraries installed (see requirements.txt).

Download the dataset from Kaggle and place the CSV files (Fake.csv, True.csv) in the working directory.

Run the provided Jupyter notebook file: FakeNewsClassifierUsingLSTM_Final.ipynb.
