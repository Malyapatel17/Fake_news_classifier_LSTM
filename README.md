# Fake News Classifier Using LSTM

This repository contains a **Fake News Detection** model built using an LSTM (Long Short-Term Memory) neural network, trained to classify news headlines as fake or real.

## 📄 Description

This project builds an LSTM-based Fake News Classifier using only headlines. It applies tokenization, stopword removal, and lemmatization with Word2Vec embeddings. Achieves ~93% accuracy with faster training. Future work includes adding full text and advanced models for better results.

## 📂 Dataset

- Dataset source: [Kaggle, Fake and True News](https://www.kaggle.com/code/therealsampat/fake-news-detection/input?select=True.csv)
- The dataset consists of two CSV files: `Fake.csv` and `True.csv`.

## 🏗️ Pipeline Overview

1. **Data Loading**
   - Load news headlines and metadata from the CSV files using pandas.

2. **Preprocessing**
   - Use the **`title`** column only.
   - Perform tokenization, stopword removal, and **lemmatization** with NLTK's `WordNetLemmatizer` to normalize text.
   - Lemmatization is preferred over stemming to better preserve word meaning.

3. **Embedding Layer**
   - Use pre-trained Word2Vec embeddings (Google News, 300 dimensions) via Gensim for improved word representation.

4. **Model Building**
   - Train an LSTM-based neural network to classify news headlines as fake or real.

5. **Evaluation**
   - Split the dataset into training and testing sets using a train-test split.
   - Evaluate accuracy and additional metrics on the test set.
   - Assess classification performance using a **confusion matrix**.
   - Additionally, conduct manual testing on custom, manually curated data samples to verify the model's behavior in practical, real-world scenarios.

## ℹ️ Important Notes & Limitations

- Only news headlines/titles are used for training and prediction; the full news text is excluded to reduce training time and resource needs.
- Despite advanced preprocessing, limited context reduces potential maximum accuracy.
- Evaluation includes a confusion matrix and manual testing on sample data to better understand strengths and weaknesses.
- Suitable for quick prototyping or when fast inference is required.

## 🔮 Future Implementation

- Combine both headlines and full news text for richer context and improved accuracy.
- Apply similar preprocessing to full text (tokenization, stopword removal, lemmatization).
- Explore advanced architectures like transformers and hybrid CNN-RNN models.
- Improve performance via transfer learning, attention mechanisms, and hyperparameter tuning.

## 🚀 How to Use

1. Clone the repository and install Python dependencies (see `requirements.txt`).
2. Download dataset CSV files (`Fake.csv`, `True.csv`) from Kaggle and place in the working directory.
3. Run the provided Jupyter notebook: `FakeNewsClassifierUsingLSTM_Final_Copy.ipynb`.


