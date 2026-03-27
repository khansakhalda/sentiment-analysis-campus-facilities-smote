# 🏫 Sentiment Analysis of Campus Facilities using Naive Bayes & SMOTE

This project focuses on analyzing student opinions regarding campus facilities at 
Universitas Jenderal Soedirman (Unsoed) using **Natural Language Processing (NLP)** 
and **Machine Learning** techniques.

The study applies **Naive Bayes Classifier** and improves its performance using 
**SMOTE (Synthetic Minority Over-sampling Technique)** to handle class imbalance.

---

## 📌 Background

Campus facilities play a crucial role in supporting student learning, comfort, 
and overall academic performance. However, evaluating facility quality manually 
from student feedback is inefficient and subjective.

With the increasing availability of textual data from surveys, **sentiment analysis** 
can be used to automatically understand student perceptions.

A common issue in sentiment classification is **class imbalance**, where one class 
(e.g., negative reviews) dominates the dataset. This imbalance can reduce model performance.

Therefore, this project utilizes **SMOTE** to balance the dataset and improve 
classification accuracy.

---

## 🎯 Objectives

This project aims to:

- Classify student feedback into **positive and negative sentiment**
- Analyze student perceptions of campus facilities
- Handle **imbalanced dataset problems** using SMOTE
- Compare model performance:
  - Without SMOTE
  - With SMOTE
- Improve classification accuracy using data-level techniques

---

## ⚙️ Process

### 1. Data Collection
- Data source: Student survey on campus facilities
- Total data: **377 responses**
- Consists of:
  - **219 negative reviews**
  - **158 positive reviews**

---

### 2. Data Preprocessing
Performed several NLP preprocessing steps:

- Cleaning (remove noise)
- Case folding
- Tokenization
- Stemming
- Stopword removal
- Labeling sentiment (positive / negative)

---

### 3. Data Splitting
- Training data: **301 samples (80%)**
- Testing data: **76 samples (20%)**

---

### 4. Feature Extraction
- Method: **TF-IDF**
- Converts text into numerical vectors
- Optimized parameters:
  - `min_df = 3`
  - `max_df = 0.25`
  - `max_features = 1000`

---

### 5. Model Development

#### 🔹 Naive Bayes (Baseline)
- Applied directly on original dataset
- Used for sentiment classification

#### 🔹 Naive Bayes + SMOTE
- SMOTE applied to balance minority class
- Generates synthetic samples
- Improves data distribution before training

---

### 6. Model Evaluation
- Evaluation metric: **Confusion Matrix**
- Accuracy comparison between:
  - Without SMOTE
  - With SMOTE

---

## 📊 Results

### 🔹 Without SMOTE
- Accuracy: **93.42%**
- Correct predictions: 71
- Errors: 5

---

### 🔹 With SMOTE
- Accuracy: **94.73%**
- Correct predictions: 72
- Errors: 4

📈 Improvement:
- Accuracy increased by **1.31%**

---

## 💡 Key Insights

- Majority of student feedback is **negative (219 vs 158)**  
  → Indicates many campus facilities still need improvement

- **Class imbalance affects model performance**, even in relatively small datasets

- Applying **SMOTE successfully improves accuracy**, although incrementally

- Naive Bayes proves to be:
  - Simple
  - Fast
  - Effective for text classification tasks

- The results highlight important issues raised by students:
  - Facility maintenance
  - Cleanliness
  - Infrastructure accessibility

📌 This insight can help universities:
- Prioritize facility improvements
- Enhance student satisfaction
- Support better learning environments

---

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- TF-IDF Vectorizer
- Imbalanced-learn (SMOTE)
- NLP preprocessing tools

---

## 👩‍💻 Author

Khansa Khalda  
Data Mining Project  
Jenderal Soedirman University
