# Building a Chatbot for Sentiment and Style Analysis

This project involves creating a chatbot designed to analyze the sentiment and style of user-provided natural language input. The chatbot's performance is determined by evaluating various machine learning models, specifically in terms of their accuracy, F1 score, precision, and recall.

## Choosing the Best Model for Training the Chatbot

After evaluating several models, the **SVM model with TF-IDF embeddings** was chosen as the best candidate for the chatbot's core sentiment and style analysis component.

### Model Selection Rationale

- **Best Performing Model on the Test Set**  
    The SVM model with TF-IDF embeddings outperforms other models with an **F1 score of 0.8129** and **accuracy of 0.8067**. These metrics suggest a strong balance between precision and recall, making it a reliable choice for accurate sentiment classification.

- **Metrics Considered in the Decision**  
    The **F1 score** and **accuracy** were the primary metrics considered:
    - The **F1 score** balances precision and recall, providing a clear measure of the model's ability to classify sentiment without overly favoring either false positives or false negatives.
    - **Accuracy** serves as a straightforward indicator of the model's overall performance.

- **Importance of These Metrics**  
    The F1 score is particularly relevant for applications where **false positives and false negatives** can affect outcomes, such as misclassifying user sentiment. For instance, mislabeling a positive review could result in missed engagement opportunities, while failing to detect a negative review could impact user feedback. Thus, both precision and recall are critical.

- **Additional Factors**  
    The TF-IDF representation was also an important factor. **TF-IDF** captures word importance effectively, allowing the SVM model to make better distinctions between sentiment polarities.

## Model Classification Report

The table below provides a comparative summary of various models evaluated in this project. Each model was tested using **TF-IDF** and **Word2Vec (w2v)** embeddings to gauge its effectiveness.

### Model Performance Summary

| Model                          | Precision   | Recall     | F1 Score   | Accuracy  |
|--------------------------------|-------------|------------|------------|-----------|
| Naive Bayes + TFIDF            | 0.5165      | 0.6351     | 0.5697     | 0.5267    |
| Naive Bayes + Word2Vec         | 0.6707      | 0.7432     | 0.7051     | 0.6933    |
| Logistic Regression + TFIDF    | 0.7381      | 0.8378     | 0.7848     | 0.7733    |
| Logistic Regression + Word2Vec | 0.7011      | 0.8243     | 0.7578     | 0.7400    |
| SVM + TFIDF                    | 0.7778      | 0.8514     | 0.8129     | 0.8067    |
| SVM + Word2Vec                 | 0.7531      | 0.8243     | 0.7871     | 0.7800    |
| Multilayer Perceptron + TFIDF  | 0.7619      | 0.8649     | 0.8101     | 0.8000    |
| Multilayer Perceptron + Word2Vec | 0.7412    | 0.8514     | 0.7925     | 0.7800    |

### Summary

The **SVM model with TF-IDF embeddings** demonstrated the highest accuracy and F1 score, making it the most effective model for this chatbot application. This combination of model and representation provides a balanced and accurate analysis of user sentiment.
