# Ethereum Fraud Detection Using Machine Learning and Deep Learning

## Overview

This major project was the final of the AI Fundamentals module for my MSc degree in computer science. It investigates the use of AI and ML techniques to detect fraudulent cryptocurrency transactions on the Ethereum blockchain.

Using real-world Ethereum transaction data, multiple machine learning and deep learning models were developed, trained and evaluated to classify transactions as either:

- 0 = Legitimate Transaction
- 1 = Fraudulent Transaction

The project compares traditional machine learning approaches with deep learning techniques to determine the most effective method for cryptocurrency fraud detection.

---

## Objectives

- Analyse a real-world Ethereum fraud dataset
- Preprocess and transform blockchain transaction data
- Engineer and select relevant features
- Train and compare multiple AI models
- Evaluate performance using fraud detection metrics
- Assess ethical considerations in AI-driven fraud detection

---

## Dataset

This project uses the Ethereum Fraud Detection Dataset sourced from Kaggle.

### Dataset Characteristics

- 9,841 Ethereum transactions
- 23 transaction-related features
- Transactions recorded between 2017 and 2023
- Binary fraud classification target variable

Example features include:

- Transaction Amount
- Gas Price
- Block Number
- Sender Address
- Receiver Address
- Gas Used

One of the primary challenges was class imbalance, with only approximately 6.5% of transactions labelled as fraudulent.

---

## Data Preprocessing

Several preprocessing techniques were applied before model training.

### Feature Engineering

- Label encoding of wallet addresses
- Correlation-based feature selection
- Numerical feature scaling using MinMaxScaler
- Cube root transformation for skewed distributions

### Class Imbalance Handling

To improve fraud detection performance, the dataset was balanced using:

- SMOTE (Synthetic Minority Oversampling Technique)
- ENN (Edited Nearest Neighbours)

These methods were combined using SMOTEENN before model training.

---

## Models Implemented

### Decision Tree

- Maximum depth of 10
- Class-weight balancing enabled
- Interpretable baseline model

### Random Forest

- Ensemble learning approach
- Bootstrap aggregation (Bagging)
- Hyperparameter tuning using RandomizedSearchCV

### Gradient Boosting (XGBoost)

- Sequential error correction
- Learning rate of 0.1
- Scale-positive-weight adjustment for class imbalance

### Multi-Layer Perceptron (MLP)

- Three hidden layers:
  - 128 neurons
  - 64 neurons
  - 32 neurons
- ReLU activation function
- Dropout regularisation

### Convolutional Neural Network (CNN)

- Two Conv1D layers
- Max pooling layers
- Dense classification layers
- Binary cross-entropy loss function

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- XGBoost
- Matplotlib
- Seaborn
- Imbalanced-Learn (SMOTEENN)

---

## Project Workflow

1. Data Collection
2. Data Exploration and Visualisation
3. Feature Engineering
4. Data Preprocessing
5. Feature Selection
6. Data Splitting (70% Training / 30% Testing)
7. Class Balancing with SMOTEENN
8. Model Training
9. Hyperparameter Tuning
10. Model Evaluation
11. Results Analysis

---

## Evaluation Metrics

Models were evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1-Score

These metrics were chosen because fraud detection problems require more than simple accuracy measurements. Precision and recall are particularly important when identifying rare fraudulent transactions.

---

## Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---------|---------|---------|---------|---------|
| Gradient Boosting | 97.5% | 92.5% | 96.5% | 94.5% |
| Random Forest | 97.0% | 90.7% | 96.5% | 93.5% |
| Decision Tree | 96.7% | 90.0% | 96.0% | 92.9% |
| CNN | 87.9% | 76.6% | 65.4% | 70.6% |
| Neural Network (MLP) | 84.8% | 96.0% | 32.9% | 49.0% |

### Best Performing Model

Gradient Boosting achieved the strongest overall performance:

- Accuracy: 97.5%
- Precision: 92.5%
- Recall: 96.5%
- F1-Score: 94.5%

The results demonstrate the effectiveness of ensemble learning techniques for detecting fraudulent cryptocurrency transactions.

---

## Key Findings

- Ensemble models outperformed deep learning models on structured transaction data.
- Gradient Boosting achieved the highest overall performance.
- Random Forest provided strong performance while remaining highly interpretable.
- Deep learning models required significantly more tuning and did not outperform ensemble approaches.
- Addressing class imbalance was critical for successful fraud detection.

---

## Ethical Considerations

The project was developed with several AI ethics principles in mind:

- Fairness and bias mitigation
- Privacy preservation through anonymised data
- Transparency and reproducibility
- Accountability and ongoing model monitoring

Future improvements could include explainability tools such as SHAP and LIME to improve transparency and trust.

---

## Future Work

Potential future improvements include:

- Real-time fraud detection systems
- Hybrid deep learning and ensemble approaches
- Explainable AI integration
- Adversarial attack resilience testing
- Multi-blockchain fraud detection (Ethereum, Bitcoin, Binance Smart Chain)

# crypto_fraud_detection
