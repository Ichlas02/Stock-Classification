# BBRI Stock Classification

This project focuses on the classification of stock performance for the BBRI (Bank Rakyat Indonesia) stock. The implementation includes data collection, preprocessing, analysis, and classification using relevant libraries and techniques.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Installation](#installation)
3. [Data Collection](#data-collection)
4. [Data Preprocessing](#data-preprocessing)
5. [Model Training and Evaluation](#model-training-and-evaluation)
6. [Results](#results)
7. [Recommendations](#recommendations)
8. [Contributors](#contributors)

## Project Overview

The notebook is a comprehensive guide for:
- Collecting news data related to BBRI using the GNews library.
- Preprocessing collected data for analysis.
- Applying machine learning or statistical models to classify stock trends.

## Installation

To run the project, you need the following dependencies:

- Python 3.x
- Libraries: Pandas, NLTK, GNews, and others (listed in the notebook).

Install required libraries:

```bash
pip install pandas nltk Gnews
```

## Data Collection

News data for BBRI is collected using the [GNews](https://pypi.org/project/Gnews/) library. This involves:
- Setting up the GNews API.
- Fetching relevant articles based on keywords.

- Total fetched data:
  
  ![image](https://github.com/user-attachments/assets/0a7ec317-49f8-431c-be32-0ab0b4ff0d51)

## Data Preprocessing

Collected data is preprocessed for analysis, including:
- Tokenization using NLTK.
- Removing irrelevant content or duplicates.

- News data preprocessing flow:
  
  ![image](https://github.com/user-attachments/assets/44c9da46-86e3-4ef0-94a7-9aaa310646bc)

- Pseudolabeling flow:
  
  ![image](https://github.com/user-attachments/assets/f9b4fa8f-c885-461f-bd46-3374a5244f9c)


## Model Training and Evaluation

This section applies machine learning models to classify stock performance. The steps include:
- Splitting data into training and test sets.
- Training the model using suitable algorithms.

- Neural network structure:

  ![image](https://github.com/user-attachments/assets/d9f27918-b19f-4bf1-a1e2-549b9e8d9a6e)

- Neural network methods used:
  - LSTM
  - Bi-LSTM
  - GRU
  - Bi-GRU
  - Voting Classifier (All Methods)
  - Voting Classifier (Bidirectionals Only)

- Feature selection scnearios:
  - RFECV
  - PCA
  - OHLCV
  - All Features
    
- Evaluating performance metrics such as accuracy.

## Results

### Sentiment Analysis
- **Best Model**: FinBERT-tone, selected for its performance in classifying stock sentiment.
- **Optimization**: Pseudolabeling on individual stocks yielded improved results, supported by iterative fine-tuning.

### Decision Signal Strategy
- **Optimal Strategy for BBRI**:
  - Target: 50 days.
  - Threshold: 11%-14%.
  - Feature: All Features
  - Labels: "Buy Weak," "Hold," "Sell Weak," and "Buy Strong."
- Achieved an average accuracy of 85.49% across all data and 87.34% for financial stocks.

### Model Evaluation
- Combined historical indicators and sentiment features, utilizing a 30-day sliding window, achieved up to 94% accuracy.
- A Voting Classifier ensemble approach proved highly effective.

### Training Results
- **Train and Validation Loss**

  ![image](https://github.com/user-attachments/assets/4043a190-922f-488b-82b9-e2d086063acd)
- **Confusion Matrix**
  
  ![image](https://github.com/user-attachments/assets/03df4096-80dd-4808-9b68-3cee3700d94f)


## Recommendations

1. Use manually labeled sentiment data to ensure a more representative dataset.
2. Adjust parameters, such as target days and thresholds, for stocks beyond BBRI.
3. Enhance sentiment features by including more granular data, such as counts of positive, negative, and neutral sentiments.

## Contributors

- **Ichlasul Hasanat**: Project Author and Developer.
