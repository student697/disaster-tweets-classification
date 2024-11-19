# Disaster Tweets Classification

## Project Overview
This project aims to classify tweets as real disaster-related or not. We experimented with multiple machine learning models to determine which approach performs best for this task, using a dataset of approximately 10,000 tweets labeled for disaster relevance.

## Dataset
- **Train Set**: 7,613 tweets, including:
  - **text**: The tweet content.
  - **target**: 1 if related to a disaster, 0 otherwise.
  
- **Test Set**: 3,263 tweets (without target labels).

## Methods Explored
We evaluated four different models:
1. **Logistic Regression**
2. **Dense Neural Network (DNN)**
3. **Long Short-Term Memory (LSTM)**
4. **1D Convolutional Neural Network (1D CNN)**

### Key Features
- **Text Preprocessing**: Standard text cleaning including tokenization, and TF-IDF feature extraction.
- **Model Training**: We split the dataset into training and validation sets (80/20 split) and evaluated models using standard metrics (accuracy, precision, recall, F1 score).
- **Evaluation Metrics**:
  - **Accuracy**: Overall classification correctness.
  - **Precision**: Fraction of correct disaster predictions.
  - **Recall**: Ability to correctly identify disaster tweets.
  - **F1 Score**: Balance of precision and recall.

## Model Performance
| Model                      | Accuracy | Precision | Recall | F1 Score |
| -------------------------- | -------- | --------- | ------ | -------- |
| Logistic Regression        | 0.7997   | 0.8221    | 0.6764 | 0.7422   |
| Dense Neural Network (DNN) | 0.7938   | 0.7933    | 0.6980 | 0.7426   |
| LSTM                       | 0.4261   | 0.4261    | 1.0000 | 0.5976   |
| 1D CNN                     | 0.7590   | 0.7252    | 0.6995 | 0.7122   |

### Summary
- **Best Model**: **Logistic Regression** performed best with a balanced precision and recall, making it suitable for our Kaggle submission.
- **DNN Performance**: Slightly lower than Logistic Regression, but still effective.
- **LSTM and 1D CNN**: Struggled to achieve higher accuracy, possibly due to insufficient training or hyperparameter tuning.
