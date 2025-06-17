# Streaming Stock Sentiment Prediction – Real-Time Spark NLP Pipeline


## ABOUT THE PROJECT:
This project implements a real-time streaming pipeline using Apache Spark to predict stock sentiment from live Twitter feeds. By combining structured financial keyword filtering with natural language processing (NLP), it enables sentiment monitoring of social media in the context of stock market fluctuations.


## USE CASE EXPLANATION:
In the financial analytics and algorithmic trading domain, public sentiment—especially on platforms like Twitter—can directly influence stock movement. This system benefits quantitative analysts, financial institutions, and retail traders by enabling real-time stock sentiment prediction for risk-aware decision-making.


## HOW IT IS BUILT AND FULL WORKING:

1. Streaming Setup:

- Simulated real-time tweets using a generator that streams JSON records (stock-relevant tweets) to a Spark socket source.

- Used Spark Structured Streaming to ingest and parse data from the socket stream.

2. Preprocessing & NLP Pipeline:

- Cleaned tweets using regex to remove hashtags, URLs, numbers, and special symbols.

- Tokenized text and applied stop word removal, lemmatization, and word embeddings.

- Implemented a TF-IDF + Logistic Regression model for sentiment classification (positive/negative).

3. Model Training & Evaluation:

- Trained sentiment classifier on a labeled dataset containing stock-relevant tweet sentiments.

- Evaluated model using accuracy, precision, recall, and F1-score.

- Integrated the trained model with the streaming pipeline for real-time predictions.

4. Dashboard Output:

- Printed real-time classified sentiments to console.

- Could be extended to push results to a dashboard or Kafka topic for downstream trading systems.


## OUTPUT AND RESULTS OR BENCHMARKS:

- Achieved real-time classification speeds under 1 second per tweet.

- Classification model reached ~85% accuracy on test data.

- Demonstrated the ability to distinguish high-volatility sentiment triggers using only short text messages.


## SKILLS, TOOLS:
Python, Apache Spark (Structured Streaming), PySpark, NLP, Logistic Regression, TF-IDF, Regex, Real-Time Processing, Twitter Simulation

## KEYWORDS:
Streaming analytics, Spark, stock sentiment, real-time NLP, financial AI, structured streaming, tweet classification, logistic regression, TF-IDF, market prediction
