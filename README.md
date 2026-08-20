# Social Media Sentiment Analysis — NLP Pipeline

## 📌 Project Overview

This project develops an end-to-end **Natural Language Processing (NLP) pipeline for Social Media Sentiment Analysis**.

The objective is to automatically classify social media posts into **Positive, Negative, and Neutral** sentiment categories. This can help businesses monitor customer opinions, identify emerging complaints, and understand sentiment trends around their products and services.

## 🎯 Business Problem

Manually monitoring thousands of social media posts is time-consuming and inefficient.

This project aims to help businesses:

* Understand customer sentiment toward products and services
* Identify negative feedback and potential issues
* Detect positive sentiment and marketing opportunities
* Support faster, data-driven customer engagement

## 🔄 Project Workflow

```text
Data Acquisition
       ↓
Data Exploration
       ↓
Data Cleaning
       ↓
Sentiment Label Normalization
       ↓
Exploratory Data Analysis
       ↓
Train/Test Split
       ↓
Text Feature Engineering
       ↓
Model Training
       ↓
Model Evaluation
       ↓
Business Recommendations
```

## 🧹 Data Preprocessing

The text preprocessing stage includes:

* Removing URLs
* Removing user mentions
* Removing hashtag symbols
* Removing unnecessary punctuation
* Removing excess whitespace
* Converting text to lowercase

The original sentiment labels are also mapped into three broader categories:

**Positive | Negative | Neutral**

## 📈 Exploratory Data Analysis

The project examines the distribution of the three sentiment classes and explores patterns within the processed social-media data.

The resulting classes contain:

| Sentiment | Records |
| --------- | ------: |
| Neutral   |     454 |
| Positive  |     211 |
| Negative  |      67 |

## 🤖 Machine Learning Models

Three text-classification approaches are implemented:

1. **Multinomial Naive Bayes + CountVectorizer**
2. **Logistic Regression + TF-IDF**
3. **Linear SVM + TF-IDF**

The dataset is divided into **80% training and 20% testing data**, using stratification to maintain class proportions.

## 📊 Model Performance

| Model                   |   Accuracy | Macro Precision | Macro Recall |   Macro F1 |
| ----------------------- | ---------: | --------------: | -----------: | ---------: |
| Multinomial Naive Bayes | **71.43%** |      **78.75%** |       53.91% | **57.48%** |
| Logistic Regression     |     62.59% |          40.89% |       34.98% |     29.72% |
| Linear SVM              |     69.39% |          45.58% |       45.91% |     44.80% |

Based on the evaluated models, **Multinomial Naive Bayes achieved the highest accuracy and macro F1-score** among the implemented models.

## 💡 Key Takeaways

* The dataset is dominated by **Neutral** sentiment.
* Multinomial Naive Bayes performed best among the implemented baseline models.
* Sentiment classification becomes challenging when the classes are imbalanced.
* Short social-media text can contain noise, slang, emojis, and other contextual information that is difficult for basic NLP models to capture.

## 🚀 Business Recommendations

* Improve sentiment labels using a manually annotated dataset.
* Monitor incoming social-media data for changes and model drift.
* Explore pretrained transformer models such as **DistilBERT** for more advanced sentiment classification.
* Improve explainability using techniques such as SHAP or class-specific n-gram analysis.

## ⚠️ Limitations

* The sentiment-label mapping uses keyword-based heuristics and may introduce noise.
* Social-media language can contain sarcasm, slang, emojis, and other contextual signals.
* The dataset is relatively small for training more complex neural NLP models.
* The current pipeline focuses on three broad sentiment categories.



## 📌 Conclusion

This project demonstrates an end-to-end NLP workflow for automatically analysing social-media sentiment. It combines text preprocessing, feature engineering, exploratory analysis, and multiple machine-learning models to transform unstructured social-media text into actionable sentiment information.



## 👤 Author

**Uha Kunapalli**
