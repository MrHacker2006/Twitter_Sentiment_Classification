# Twitter Sentiment Classification using Random Forest

This project performs binary sentiment analysis (positive or negative) on tweets using a subset of the **Sentiment140** dataset and a **Random Forest classifier**. The model classifies the sentiment of a given tweet based on its textual content.

---

## 📁 Dataset

- **Source:** [Sentiment140](http://help.sentiment140.com/for-students)
- **Subset used:** 100,000 rows from the original dataset.
- **Columns Used:**
  - `sentiment`: 0 (negative) or 4 (positive), converted to 0 and 1
  - `tweet`: The tweet text

---

## ⚙️ Workflow

1. **Data Cleaning (No NLTK)**  
   - Removes URLs, mentions, hashtags, punctuation, numbers
   - Converts text to lowercase

2. **Feature Extraction**  
   - TF-IDF Vectorizer (top 5000 features)

3. **Label Encoding**  
   - Converts sentiments to numeric labels

4. **Model Training**  
   - Random Forest Classifier with 100 estimators

5. **Evaluation**  
   - Accuracy, Confusion Matrix, Classification Report

6. **Prediction on New Tweet**  
   - A sample tweet is cleaned, vectorized, and passed to the model for prediction

---

## 📦 Dependencies

- pandas  
- scikit-learn  
- re (regex, standard library)

Install dependencies (if needed):

```bash
pip install pandas scikit-learn
```

---

## 🚀 How to Run

1. Place `Sentiment140_subset.csv` in the same directory.
2. Run the Python script.

```bash
python sentiment_classifier.py
```

---

## 📝 Example Output

```text
Accuracy: 0.7564

Confusion Matrix:
[[7802 1144]
 [2350 8704]]

Classification Report:
              precision    recall  f1-score   support

           0       0.77      0.87      0.81      8946
           1       0.88      0.79      0.83     11054

    accuracy                           0.82     20000
   macro avg       0.82      0.83      0.82     20000
weighted avg       0.83      0.82      0.82     20000

📝 Tweet: What an amazing sunset today! Nature is truly beautiful 🌅💛  
📊 Predicted Sentiment: positive
```

---

## 🔍 File Structure

```
sentiment_classifier.py
Sentiment140_subset.csv
README.md
```

---

## ✅ Status

- ✅ Model trained successfully  
- ✅ Works without NLTK  
- ✅ Includes real-time prediction example  
- ❌ No GUI or web interface yet

---

## 👨‍💻 Author

Gautam  
Project: **Twitter_Sentiment_Classification_M1**

---
