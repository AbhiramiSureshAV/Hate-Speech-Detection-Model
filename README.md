# Hate-Speech-Detection-Model

Overview:
This project focuses on building a hate speech detection model using machine learning techniques. The model is trained to classify text data into categories of hate speech and non-hate speech (normal speech).

Dataset:
The training and testing datasets are provided in CSV format. The training dataset (train.csv) consists of labeled text data, where each sample is associated with a label indicating whether it contains hate speech (1) or not (0). The testing dataset (test.csv) contains unlabeled text data that will be used to evaluate the performance of the trained model.

Data Preprocessing:
Before training the model, the text data undergoes preprocessing steps to clean and prepare it for analysis. The following preprocessing steps are applied:

Text is converted to lowercase.
Special characters, URLs, Twitter usernames, and other non-alphanumeric characters are removed using regular expressions.
Data Balancing:
To address class imbalance in the training dataset, the minority class (hate speech) is upsampled using the Synthetic Minority Over-sampling Technique (SMOTE). This ensures a balanced representation of both classes in the training data, which helps improve the model's performance.

Model Training:
The hate speech detection model is built using a pipeline consisting of the following components:

CountVectorizer: Converts text data into a matrix of token counts.
TfidfTransformer: Transforms the count matrix into a normalized term-frequency times inverse document-frequency (TF-IDF) representation.
SGDClassifier: A linear classifier trained using Stochastic Gradient Descent (SGD) optimization.
The model is trained on the upsampled training dataset using the pipeline. After training, the model is evaluated on a holdout test set to assess its performance.

Model Evaluation:
The performance of the hate speech detection model is evaluated using the F1 score metric. The F1 score provides a balance between precision and recall, making it suitable for imbalanced datasets. The F1 score achieved by the trained model on the test set is approximately 0.97, indicating a high level of accuracy in classifying hate speech.

We got an F1 score of 97%

Conclusion
The hate speech detection model demonstrates promising results in accurately identifying instances of hate speech in text data. With further refinement and optimization, the model can be deployed in real-world applications to monitor and mitigate the spread of hate speech online.
