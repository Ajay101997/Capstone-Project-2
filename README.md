# Capstone-Project-2
# Sentiment Analysis on E-commerce Product Reviews using NLP

## Project Overview

This project focuses on **Sentiment Analysis** of customer product reviews using **Natural Language Processing (NLP)**, **Machine Learning**, and **Deep Learning** techniques.

Customer reviews are valuable sources of feedback for businesses. However, manually analyzing thousands of reviews is time-consuming and inefficient. This project develops an automated sentiment classification system that predicts whether a review is **Positive**, **Negative**, or **Neutral**.

---

# Problem Statement

Customer reviews are available in large volumes and are stored as unstructured text data. Manual analysis of these reviews is difficult, time-consuming, and prone to errors.

The objective of this project is to build an automated NLP-based system capable of classifying customer reviews into Positive, Negative, and Neutral sentiments.

---

# Objectives

- Perform sentiment analysis on customer reviews.
- Clean and preprocess textual data.
- Convert text into numerical features.
- Handle imbalanced data.
- Train Machine Learning and Deep Learning models.
- Compare model performance.
- Predict sentiment for unseen customer reviews.

---

# Dataset

The project consists of three datasets.

| Dataset | Description |
|---------|-------------|
| **train_data.csv** | Used to train the models |
| **test_data.csv** | Used to evaluate model performance |
| **hidden_data.csv** | Used for final sentiment prediction |

### Important Columns

- **reviews.text** → Customer review
- **sentiment** → Target class (Positive, Negative, Neutral)

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- NLTK
- Regular Expressions (Regex)
- Scikit-learn
- TensorFlow / Keras
- Imbalanced-learn

---

# Exploratory Data Analysis (EDA)

EDA was performed to better understand the dataset before model building.

## 1. Sentiment Distribution

<img width="700" height="400" alt="sentiment_distribution" src="https://github.com/user-attachments/assets/f2f4595c-724d-4a04-855e-5fad46a66381" />

### Observation

- Positive reviews dominate the dataset.
- Neutral and Negative reviews are comparatively fewer.
- The dataset is imbalanced, so Random Over Sampling was applied.

---

## 2. Review Length Distribution

<img width="700" height="400" alt="review Length Distribution" src="https://github.com/user-attachments/assets/80a3434b-8a7c-4406-9a47-8697258905e9" />

### Observation

- Most customer reviews are short to medium in length.
- Only a small number of reviews are very long.
- This helped determine the maximum sequence length for the LSTM model.

---

## 3. Top 10 Most Common Words

<img width="700" height="400" alt="top_words" src="https://github.com/user-attachments/assets/9ed502d7-c07c-4f45-a665-37897858412a" />

### Observation

- The bar chart displays the ten most frequently occurring words after text preprocessing.
- These words provide insight into common topics discussed by customers.

---

#  Data Preprocessing

The following preprocessing techniques were applied:

- Removed duplicate records
- Handled missing values
- Converted text to lowercase
- Removed punctuation
- Removed numbers
- Removed special characters
- Tokenization
- Stopword removal
- Text cleaning using Regular Expressions

---

#  Feature Engineering

### Machine Learning

- TF-IDF Vectorization

### Deep Learning

- Tokenizer
- Padding Sequences

---

#  Handling Imbalanced Data

Since the dataset contained more Positive reviews than other classes, **Random Over Sampling** was applied to balance the sentiment classes before model training.

---

# Models Implemented

## Machine Learning

- Multinomial Naive Bayes
- Linear Support Vector Machine (Linear SVM)

## Deep Learning

- Long Short-Term Memory (LSTM)

---

#  LSTM Architecture

- Embedding Layer
- LSTM Layer (64 Units)
- Dropout Layer (0.5)
- Dense Layer (Softmax Activation)

---

#  Model Evaluation

The models were evaluated using:

- Accuracy Score
- Classification Report
- Confusion Matrix
- Training Accuracy
- Validation Accuracy
- Training Loss
- Validation Loss

---

## Confusion Matrix (Linear SVM)

<img width="700" height="400" alt="confusion_matrix_svm" src="https://github.com/user-attachments/assets/fb0deeff-7b06-49d5-ab5b-072b7cfac7e2" />

### Observation

- The confusion matrix indicates that the Linear SVM correctly classified most customer reviews.
- Only a small number of reviews were misclassified, demonstrating strong predictive performance.

---

## LSTM Training Accuracy

<img width="700" height="400" alt="lstm_accuracy" src="https://github.com/user-attachments/assets/501b6c01-946c-4525-8efc-eb16b79e47e7" />

### Observation

- Training and validation accuracy improved across epochs.
- The close alignment between both curves indicates good learning without significant overfitting.

---

## LSTM Training Loss

<img width="700" height="400" alt="lstm_loss" src="https://github.com/user-attachments/assets/c3cc9c5f-64c8-4215-bd3c-37bf847fd3a3" />

### Observation

- Training and validation loss decreased steadily during training.
- This suggests that the model successfully minimized prediction errors and converged effectively.

---

# Model Comparison

| Model | Status |
|--------|--------|
| Multinomial Naive Bayes | Implemented |
| Linear SVM | Implemented |
| LSTM | Implemented |

## Best Performing Model

**Linear Support Vector Machine (Linear SVM)**

### Reasons

- High classification accuracy
- Fast training time
- Excellent performance with TF-IDF features
- Well-suited for high-dimensional text classification

---

# Final Prediction

The best-performing model was used to predict sentiment for the hidden dataset.

Prediction results were exported as:

```text
final_predictions.csv
```

---

# Project Structure

```text
Sentiment-Analysis-Ecommerce-Reviews/
│
├── datasets/
│   ├── train_data.csv
│   ├── test_data.csv
│   └── hidden_data.csv
│
├── images/
│   ├── sentiment_distribution.png
│   ├── review_length_distribution.png
│   ├── top_words.png
│   ├── confusion_matrix_svm.png
│   ├── lstm_accuracy.png
│   └── lstm_loss.png
│
├── Sentiment_Analysis.ipynb
├── final_predictions.csv
├── requirements.txt
└── README.md
```

---

# Future Scope

- Improve performance using Transformer-based models such as **BERT**
- Apply Hyperparameter Tuning
- Deploy the model using **Streamlit** or **Flask**
- Integrate the system into real-time review monitoring applications

---

# Learning Outcomes

Through this project, I gained practical experience in:

- Natural Language Processing (NLP)
- Text preprocessing
- TF-IDF feature extraction
- Handling imbalanced datasets
- Machine Learning algorithms
- Deep Learning with LSTM
- Model evaluation
- Sentiment prediction on unseen customer reviews

---

# Installation

Clone the repository:

```bash
git clone https://github.com/Ajay101997/Capstone-Project-2.git
```

Move into the project directory:

```bash
cd Sentiment-Analysis-Ecommerce-Reviews
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

---

# 👨‍💻 Author

**Ajay Kumar Sahu**

GitHub: https://github.com/Ajay101997/Capstone-Project-2.git

LinkedIn: www.linkedin.com/in/ajay-kumar-sahu-68804621b
