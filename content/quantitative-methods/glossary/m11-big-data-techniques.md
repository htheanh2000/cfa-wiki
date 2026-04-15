---
title: "Glossary: M11 — Big Data and Machine Learning"
type: glossary
subject: quantitative-methods
module: M11
created: 2026-04-09
updated: 2026-04-09
tags: [glossary, big-data, machine-learning, AI, fintech, NLP]
---

# Glossary: M11 — Big Data and Machine Learning

**Module**: [[quantitative-methods/modules/m11-big-data-techniques/index|M11]]
**Concept page**: [[quantitative-methods/concepts/big-data-and-ml|Big Data and ML Concept]]

---

## Fintech

Financial technology — the application of technology and innovation to financial services. Encompasses areas such as digital payments, robo-advisors, algorithmic trading, blockchain, and [[#Machine Learning (ML)]]-driven investment analysis.

**LOS**: 11.a | **Related**: [[quantitative-methods/concepts/big-data-and-ml|Big Data and ML Concept]]

---

## Big Data

Extremely large and complex data sets that cannot be processed with traditional data management tools. Characterized by the "Vs": [[#Volume]], [[#Velocity]], [[#Variety]], and [[#Veracity]].

**LOS**: 11.b | **Related**: [[#Traditional Data]], [[#Alternative Data]]

---

## Volume

One of the characteristics of [[#Big Data]]. Refers to the enormous quantity of data being generated — vastly exceeding what traditional databases can store and process (terabytes to petabytes and beyond).

**LOS**: 11.b

---

## Velocity

One of the characteristics of [[#Big Data]]. Refers to the speed at which data is generated, collected, and processed. Real-time data streams (e.g., market tick data, social media feeds) exemplify high velocity.

**LOS**: 11.b

---

## Variety

One of the characteristics of [[#Big Data]]. Refers to the many different forms of data — [[quantitative-methods/glossary/m03-statistical-measures#Structured Data|structured]] (databases), [[quantitative-methods/glossary/m03-statistical-measures#Unstructured Data|unstructured]] (text, images, audio), and semi-structured (XML, JSON).

**LOS**: 11.b | **Related**: [[quantitative-methods/glossary/m03-statistical-measures#Structured Data|Structured Data]], [[quantitative-methods/glossary/m03-statistical-measures#Unstructured Data|Unstructured Data]]

---

## Veracity

One of the characteristics of [[#Big Data]]. Refers to the uncertainty, noise, and reliability concerns associated with large data sets. Big data often contains errors, inconsistencies, and incomplete records.

**LOS**: 11.b

---

## Traditional Data

Data collected by companies via standardized processes and reported on a regular schedule. Historically the primary source for investment analysis.

**LOS**: 11.c | **Examples**: Financial statements, economic statistics, exchange-traded price and volume data. | **Contrast**: [[#Alternative Data]]

---

## Alternative Data

Data generated from non-traditional sources. Can reveal information about a company's performance or economic conditions before it is reflected in traditional data or reported financials.

**LOS**: 11.c | **Examples**: Satellite imagery of parking lots, credit card transaction data, social media sentiment, web scraping data. | **Related**: [[#Big Data]], [[#Text Analytics]]

---

## Data Processing Pipeline

The sequential set of steps used to transform raw data into a form suitable for analysis: collection → cleansing → preprocessing → feature engineering → model application → output.

**LOS**: 11.d | **Relevance to investment analysis**: Data quality and pipeline integrity are critical; garbage in, garbage out.

---

## Artificial Intelligence (AI)

The simulation of human intelligence processes by computer systems. Encompasses learning, reasoning, and self-correction. Includes [[#Machine Learning (ML)]] and [[#Deep Learning]] as subfields.

**LOS**: 11.e | **In finance**: Algorithmic trading, fraud detection, credit scoring, robo-advisory services.

---

## Neural Network

A machine learning model loosely inspired by the human brain, consisting of layers of interconnected nodes (neurons). Identifies complex patterns in data through multiple layers of transformation.

**LOS**: 11.e | **Foundation for**: [[#Deep Learning]] (neural networks with many hidden layers). | **Related**: [[#Machine Learning (ML)]]

---

## Machine Learning (ML)

A subset of [[#Artificial Intelligence (AI)]] in which systems learn from data to improve performance on a task without being explicitly programmed with rules. Divided into [[#Supervised Learning]], [[#Unsupervised Learning]], and reinforcement learning.

**LOS**: 11.e | **In finance**: Signal generation, risk management, fraud detection, portfolio optimization.

---

## Supervised Learning

A machine learning approach where the algorithm is trained on a labeled data set — each input has a known, correct output (label). The model learns to map inputs to outputs.

**LOS**: 11.f | **Applications**: Credit default prediction (classify: default/no default), return forecasting (predict: continuous return). | **Related**: [[#Training Dataset]], [[#Overfitting]]

---

## Unsupervised Learning

A machine learning approach where the algorithm finds patterns in data without labeled examples. Discovers hidden structure in unlabeled data.

**LOS**: 11.f | **Applications**: Clustering stocks by return behavior; anomaly detection; topic modeling in financial news. | **Contrast**: [[#Supervised Learning]]

---

## Deep Learning

A subset of [[#Machine Learning (ML)]] using [[#Neural Network|neural networks]] with many layers (deep architectures). Able to learn hierarchical representations from raw data without manual feature engineering.

**LOS**: 11.f | **Applications**: [[#Natural Language Processing (NLP)]], image recognition (satellite imagery), speech recognition. | **Key limitation**: Computationally intensive; requires large amounts of data.

---

## Training Dataset

The portion of the data used to fit (train) a machine learning model — i.e., to estimate the model's parameters.

**LOS**: 11.g | **Related**: [[#Validation Dataset]], [[#Testing Dataset]], [[#Overfitting]]

---

## Validation Dataset

A subset of data held out from training, used to tune model hyperparameters and select the best model during development. Provides an estimate of model performance during model selection.

**LOS**: 11.g | **Key distinction**: Used during model building, unlike the [[#Testing Dataset]] which is used only for final evaluation.

---

## Testing Dataset

A subset of data held out entirely from model development, used only for final evaluation of model performance on unseen data. Provides an unbiased estimate of generalization error.

**LOS**: 11.g | **Warning**: If the testing set is used repeatedly, it effectively becomes part of the training process → contamination bias.

---

## Overfitting

A modeling problem where the model captures the noise and idiosyncrasies of the training data rather than the underlying true relationship. Performs well on training data but poorly on new data.

**LOS**: 11.g | **Cause**: Model is too complex (too many parameters) relative to the amount of training data. | **Remedy**: Regularization, cross-validation, larger data sets. | **Contrast**: [[#Underfitting]]

---

## Underfitting

A modeling problem where the model is too simple to capture the true relationship in the data. Performs poorly on both training and new data.

**LOS**: 11.g | **Cause**: Model is too constrained (too few parameters or too rigid). | **Contrast**: [[#Overfitting]]

---

## Black Box

Describes machine learning models (particularly [[#Deep Learning]]) whose internal workings are difficult or impossible to interpret, even though their predictions may be accurate.

**LOS**: 11.h | **Concern in finance**: Regulatory requirements and risk management demand model explainability; black-box models make it difficult to audit decisions or explain outcomes to clients.

---

## Text Analytics

The process of deriving structured, quantitative information from unstructured text data using computational methods. Encompasses [[#Natural Language Processing (NLP)]] and [[#Sentiment Analysis]].

**LOS**: 11.i | **Application**: Mining analyst reports, earnings call transcripts, regulatory filings, and news articles for investment signals. | **Related**: [[quantitative-methods/glossary/m03-statistical-measures#Unstructured Data|Unstructured Data]]

---

## Natural Language Processing (NLP)

A field of [[#Artificial Intelligence (AI)]] focused on enabling computers to understand, interpret, and generate human language. Underpins [[#Text Analytics]] and [[#Sentiment Analysis]].

**LOS**: 11.i | **Techniques**: Tokenization, named entity recognition, topic modeling, word embeddings. | **Application**: Processing earnings calls, news feeds, and SEC filings.

---

## Sentiment Analysis

The use of [[#Natural Language Processing (NLP)]] to identify and quantify the emotional tone (positive, negative, neutral) of text data. Used to assess market sentiment from news and social media.

**LOS**: 11.i | **Application**: Extracting forward-looking indicators from management commentary; monitoring social media for signals on consumer sentiment.
