# Duplicate_Question_Pair_Classifier

This project implements a classifier for detecting duplicate question pairs using Word2Vec for feature extraction, and XGBoost and Random Forest classifiers for prediction. The classifier incorporates various custom features such as question length, word count, common words, and word share to improve classification accuracy.  

## Dataset

This model is designed to work with question pairs labeled as duplicate or non-duplicate. The dataset should contain:  

1. question1: The first question in the pair  
2. question2: The second question in the pair  
3. is_duplicate: A binary label (1 for duplicate, 0 for non-duplicate)

## Model

The classifier uses Word2Vec for feature extraction to convert the questions into numerical vectors that can be used by machine learning models. The following custom features are used for classification:  

### Length Based Features
1. Length of q1: The number of characters in the first question.  
2. Length of q2: The number of characters in the second question.  
3. Number of words in q1: The word count in the first question.  
4. Number of words in q2: The word count in the second question.  
5. Number of common words: The count of words that appear in both questions.  
6. Total words (q1 + q2): The total word count across both questions.  
7. Word share: The ratio of common words to the total number of words in both questions.  

### Token Features
These features are based on the tokenized representation of the questions. They provide insights into the structure and similarity of the questions based on their word content.  

### Machine Learning Algorithms:

1. Random Forest Classifier: Achieved an accuracy of 83%.  
2. XGBoost Classifier: Achieved an accuracy of 82.5%.  

## Evaluation
The performance of the model is evaluated using standard metrics like accuracy. The Random Forest model achieved 83% accuracy, while the XGBoost model achieved 82.5% accuracy.
