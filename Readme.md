# Building the Chatbot for analyzing the sentiment and style of user-provided natural language input

### Chosing the model best suited for training the chatbot


- **Which model do you think performs best on the test set?**
    - The SVM model with TF-IDF seems to perform the best on the test set. It has the highest **F1 score (0.8129)** and **accuracy (0.8067)**, which indicates a strong balance between precision and recall.
- **Which metric(s) did you base your decision on?**
    - I primarily based my decision on the F1 score and accuracy. The F1 score is critical as it considers both precision and recall, offering a balanced measure of a model’s ability to classify positive and negative cases correctly. Accuracy was also a consideration as it provides a clear indication of how often the model makes correct predictions overall.
- **Why did you decide that these metrics were most important for this task?**
    - The F1 score is particularly important in scenarios where both **false positives and false negatives** can have significant consequences, like in . For example, incorrectly classifying a positive review as negative could affect user engagement, and missing a genuinely positive review could result in lost opportunities for feedback. Therefore, balancing precision and recall is crucial. Accuracy is also relevant since it provides a straightforward understanding of the model's general performance.
- **Were there any other factors in your decision to select this model going forward for use in your chatbot?**
    - Besides the metrics, I also considered the representation used (TF-IDF). TF-IDF provides a reliable understanding of word importance in the context of sentiment analysis, allowing SVM to better distinguish between positive and negative reviews.