# Spam Classifier Analysis Project

## Project Overview

This project implements a spam classifier that uses machine learning to automatically detect and filter spam messages from legitimate (ham) messages. The goal is to build a simple yet effective text classification model using the Naive Bayes algorithm, demonstrating how machines can learn to distinguish between genuine and unwanted communications.

## Introduction

Spam messages are a persistent problem in digital communication, ranging from phishing attempts to unwanted advertisements. This project explores how a machine learning model can be trained to classify text messages as either "ham" (legitimate) or "spam" (junk) using natural language processing techniques. The classifier processes raw text, converts it into numerical representations, and applies probabilistic learning to make predictions.

## Datasets

- **Source:** Personal data created for this project
- **Description:** The dataset contains 30 labeled text messages — 15 ham (legitimate) and 15 spam (junk) examples
- **Format:** CSV with two columns: `text` (message content) and `label` (ham/spam)
- **Why:** A small, controlled dataset was used to clearly demonstrate the classification pipeline and observe how the model behaves with different training/test splits

## Methodology / Algorithm

1. **Data Preparation:** The dataset is loaded into a Pandas DataFrame for easy manipulation
2. **Train-Test Split:** The data is split into training and testing sets using `train_test_split` with stratified sampling to maintain class balance
3. **Vectorization:** Text messages are converted into numerical feature vectors using `CountVectorizer`, which counts word occurrences to create a bag-of-words representation
4. **Model Training:** A `MultinomialNB` (Multinomial Naive Bayes) classifier is trained on the vectorized training data. Naive Bayes is well-suited for text classification as it calculates the probability of each class given the word features
5. **Evaluation:** The model's performance is measured using accuracy score and a detailed classification report (precision, recall, F1-score)

## Tech Stack

- **Environment:** Google Colab / VS Code
- **Language:** Python 3.13.5
- **Libraries:**
  - `pandas` — Data manipulation and analysis
  - `scikit-learn` — Machine learning tools (CountVectorizer, MultinomialNB, train_test_split, accuracy metrics)

## Observations / Findings

The classifier was tested across four different test split sizes to observe how data distribution affects performance:

| Test Size | Test Samples | Accuracy |
|-----------|-------------|----------|
| 0.1 | 3 | 100.00% |
| 0.2 | 6 | 83.33% |
| 0.3 | 9 | 88.89% |
| 0.4 | 12 | 83.33% |

**Key Findings:**
- The `0.1` split achieved 100% accuracy but with only 3 test samples, making it unreliable
- The `0.3` split provided the best balanced result at 88.89% accuracy
- The classifier was consistently better at identifying ham messages than spam
- Subtle promotional messages (discounts, offers) were sometimes misclassified as ham, while obvious spam with urgent language was correctly detected
- Overall accuracy remained above 83% across all meaningful test sizes, demonstrating the viability of the Naive Bayes approach for spam detection

## Contributor / Creator

**Lavhelani Mano**
Computer Science Honours Student
University of the Western Cape

## References

- Source I: Scikit-learn Documentation — https://scikit-learn.org/stable/
- Source II: Pandas Documentation — https://pandas.pydata.org/docs/
