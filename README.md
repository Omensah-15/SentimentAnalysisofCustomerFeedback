# Customer Feedback Sentiment Analysis Using NLP

This project focuses on analyzing customer sentiments from feedback collected across multiple platforms using natural language processing (NLP). The goal is to classify feedback as **Positive** or **Negative**, visualize patterns across **location**, **platform**, and **confidence scores**, and derive insights that can help businesses improve their services and engagement strategies.

---

## Dataset Overview

The dataset contains **1000 synthetic customer feedback entries** across platforms such as **Yelp, Amazon, IMDb, Spotify, Online Stores**, and more. Each record includes sentiment labels and a confidence score for how certain the model is about the classification.

### Dataset Columns:

| Column             | Description                                                   |
|--------------------|---------------------------------------------------------------|
| `Text`             | Raw customer feedback                                          |
| `Sentiment`        | Predicted sentiment — `Positive` or `Negative`                |
| `Source`           | Platform the feedback was collected from                      |
| `Date/Time`        | Timestamp of when the feedback was given                      |
| `User ID`          | Anonymized unique identifier for users                        |
| `Location`         | Geographical location of the user                             |
| `Confidence Score` | Model's confidence (0.00 to 1.00) in the sentiment prediction |

---

## Data Cleaning & Preprocessing

1. **Missing Data Check & Removal**
   - Checked for missing values in all columns.
   - Dropped or imputed missing values to ensure data consistency.

2. **Datetime Conversion**
   - Parsed `Date/Time` to Python datetime objects for time-based analysis.

3. **Text Cleaning**
   - Lowercased all feedback.
   - Removed special characters, numbers, and extra whitespace.
   - Removed stopwords and performed **lemmatization** using spaCy/NLTK.

4. **Encoding & Formatting**
   - Encoded sentiment as binary values (0 for Negative, 1 for Positive) if needed.
   - Standardized column formats and ensured data types were appropriate.

---

## 📈 Exploratory Data Analysis (EDA)

### 📌 Sentiment Distribution

- **Positive Sentiment Count:** 52%
- **Negative Sentiment Count:** 48%

```text
Positive    52
Negative    43
```

> **Insight:** Feedback is relatively balanced, with a slight lean toward positive responses.

---

### ✅ Confidence Score Insights

- **Overall Mean Confidence Score:** `0.791`
- **Positive Sentiment Avg. Confidence:** `0.905`
- **Negative Sentiment Avg. Confidence:** `0.653`

> **Insight:** The model shows high confidence when predicting **positive sentiments**, suggesting they are more clearly expressed compared to negative feedback.

---

## 🏷️ Sentiment by Source

| Source              | Negative | Positive |
| ------------------- | -------- | -------- |
| Amazon Reviews      | 2        | 0        |
| IMDb                | 1        | 5        |
| TripAdvisor         | 0        | 6        |
| Spotify             | 0        | 9        |
| Website Testimonial | 0        | 4        |
| Yelp Reviews        | 4        | 2        |
| Online Store        | 10       | 1        |
| Website Review      | 7        | 0        |
| Zomato              | 6        | 1        |
| Online Forum        | 2        | 0        |
| Hotel Review        | 2        | 0        |
| Online Helpdesk     | 2        | 0        |
| Goodreads           | 2        | 4        |

> **Insight:**
>
> - Platforms like **Spotify, TripAdvisor, and IMDb** receive overwhelmingly **positive feedback**.
> - Sources such as **Online Stores, Yelp, Website Reviews, and Zomato** are **dominated by negative feedback**, indicating customer dissatisfaction in digital retail and food delivery spaces.

---

## 🌍 Sentiment by Location

| Location      | Negative | Positive |
| ------------- | -------- | -------- |
| Berlin        | 0        | 10       |
| Chicago       | 5        | 0        |
| London        | 2        | 9        |
| Los Angeles   | 7        | 2        |
| Mumbai        | 6        | 2        |
| New York      | 0        | 7        |
| Orlando       | 0        | 5        |
| Paris         | 3        | 7        |
| San Francisco | 8        | 0        |
| Sydney        | 3        | 9        |
| Toronto       | 9        | 1        |

> **Insight:**
>
> - **Berlin, Orlando, New York, and Sydney** have mostly **positive feedback**.
> - **San Francisco, Toronto, Chicago**, and **Los Angeles** had the most **negative sentiment**, suggesting potential customer experience issues in these areas.

---

## 📊 Average Confidence Score by Location

| Location      | Avg. Confidence Score |
| ------------- | --------------------- |
| Orlando       | 0.912                 |
| Berlin        | 0.907                 |
| New York      | 0.883                 |
| London        | 0.864                 |
| Sydney        | 0.824                 |
| Paris         | 0.816                 |
| San Francisco | 0.701                 |
| Los Angeles   | 0.701                 |
| Toronto       | 0.697                 |
| Mumbai        | 0.696                 |
| Chicago       | 0.668                 |

> **Insight:**
>
> Locations like **Orlando, Berlin, and New York** show **high model confidence**, likely due to more expressive or clearer reviews. In contrast, locations with **lower confidence** scores like **Chicago** and **Toronto** may include more ambiguous or mixed-sentiment feedback.

---

## 🧰 Tools & Technologies Used

- **Python**: Core programming language for data processing
- **Pandas & NumPy**: Data manipulation and analysis
- **Matplotlib & Seaborn**: Visualization libraries
- **NLTK / spaCy**: Natural Language Processing (Text Cleaning, Lemmatization)
- **Jupyter Notebook**: Development environment

---

## 🧠 Business Insights

- **Retail & Service Businesses**: Feedback from platforms like **Amazon, Online Stores, and Yelp** shows recurring negative sentiments — a signal for those businesses to reassess service quality and support responsiveness.
- **Media & Entertainment**: High positivity from **Spotify and IMDb** indicates strong user satisfaction — good for maintaining current customer engagement strategies.
- **Location-Specific Insights**: Poor sentiment in **San Francisco and Toronto** could guide regional marketing or product experience improvements.
- **Customer Experience Strategy**: Combining sentiment with confidence scores and feedback source allows for **data-driven prioritization** of problem areas.

---

## ✅ Conclusion

This sentiment analysis project not only demonstrates NLP application in real-world feedback but also delivers actionable insights for customer experience teams. By understanding which platforms and locations foster positive vs negative sentiment, businesses can better tailor support, communication, and service improvements.

---
## 👨‍💻 Author

**Obed Mensah**  
*Data Scientist — Python | Power BI | SQL | Analytics*  
📧 [heavenzlebron7@gmail.com](mailto:heavenzlebron7@gmail.com)
