# Sentiment_Analysis
Sentiment Analysis of TripAdvisor Hotel Reviews

This project focuses on sentiment analysis using hotel reviews from TripAdvisor. The analysis employs the VADER sentiment analyzer from the NLTK library to score and interpret the sentiment of each review. Below is a detailed overview of the project workflow and key steps.

## Dataset

- Source: Kaggle - TripAdvisor Hotel Review Sentiment Analysis
- File: b.csv
- Encoding: ISO-8859-1

## Data Overview

```python df.head(10)```

Sample data preview of the first 10 rows.

## Handling Missing Values

```python
null_values = df.isnull()
null_counts = null_values.sum()
```

Count of missing values in each column.

Data Subset for Analysis


## Distribution of Ratings
```python
A bar chart visualizes the distribution of star ratings:

ax = df['Rating'].value_counts().sort_index().plot(kind='bar', title='Count of Reviews by Stars', figsize=(10, 5))
ax.set_xlabel('Star Rating')
ax.set_ylabel('Count')
plt.show()
```

## Sentiment Analysis with NLTK

NLTK Downloads

Essential NLTK resources are downloaded:
```python
nltk.download('vader_lexicon')
nltk.download('words')
nltk.download('maxent_ne_chunker')
nltk.download('punkt')
nltk.download('averaged_perceptron_tagger')
```

## Tools and Libraries

Python

Pandas

Numpy

Matplotlib

Seaborn

NLTK

tqdm

## Summary

This project demonstrates fundamental sentiment analysis techniques using VADER and visualizes the relationship between review sentiment and ratings. Future steps could include using other models and fine-tuning for more robust sentiment detection.

