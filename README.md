# Sentiment Analysis Using Federated Learning

This project performs sentiment analysis using federated learning on the Sentiment140 dataset, which contains 1.6 million records.

## 📄 Project Workflow:

### Data Preprocessing:
- Cleaned and prepared the dataset.
- Due to Kaggle's package restrictions (unable to import contractions), data preprocessing was done in Google Colab.

### Data Splitting:
- Divided the preprocessed data into 4 parts:
  - 3 parts for 3 different clients (approximately 1.2 million records).
  - 1 part for testing (approximately 0.4 million records).

### Embedding Layer:
- Used GloVe.6B.100d pre-trained word embeddings to represent the text data.

### Training:
- Trained the model using Federated Learning across 3 clients on Kaggle.
- Kaggle was chosen for training because it supports running multiple clients simultaneously.

### Testing and Evaluation:
- Evaluated the model trained on 1.2 million records using accuracy on the test set (0.4 million records).
- For quick validation, sample datasets were used during training and testing to print Accuracy, Precision, Recall, and F1-score.

## 📊 Results:
The global model's performance was reported after every communication round.  
Final evaluation metrics include:
- Accuracy (for the model trained on 1.2 million records)
- Precision
- Recall
- F1-score

**Note:** Accuracy will be printed for both models, whereas Precision, Recall, and F1-score will be printed only for the model trained and tested on the sample dataset.

## 🛠️ Technologies Used:
- Python
- TensorFlow
- Flower (for federated learning)
- Kaggle (for training)
- Google Colab (for preprocessing)
- GloVe.6B.100d (for word embeddings)

## 🔄 How to Run:
1. Run the data preprocessing code in Google Colab.
2. Upload the 1.6 million records file to Google Colab before running the code (e.g., `training_data`).
3. After running the preprocessing code, you will get the client and test files downloaded.
4. Go to Kaggle and paste the Sentiment Analysis using Federated Learning code.
5. Upload the client and test data files to Kaggle and also upload the GloVe.6B.100d embedding file.
6. When prompted for the database name, you can name it as per your preference (e.g., `dataset-sentiment140`).
   - Make sure to adjust the data path in the code according to your dataset name.
7. Verify your Kaggle account with your phone number to use the GPU (P100).
8. Select the latest environments and run the code.
9. Your global accuracy will be printed after each round.
10. If you'd like to get Precision, Recall, and F1-score, use the `SentimentAnalysis_accuracy_precision_recall_f1-score` code for sample dataset.
