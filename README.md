# Spam-Email-Classifier
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spam Detection using Naive Bayes</title>
</head>
<body>
    <h1>Spam Detection using Naive Bayes</h1>
    <p>This project demonstrates how to build a spam detection system using the Naive Bayes algorithm. The dataset used contains SMS messages labeled as "spam" or "ham" (not spam). The model is trained to classify messages into these categories.</p>

    <h2>Table of Contents</h2>
    <ul>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#dataset">Dataset</a></li>
        <li><a href="#steps">Steps</a></li>
        <li><a href="#results">Results</a></li>
        <li><a href="#usage">Usage</a></li>
    </ul>

    <h2 id="installation">Installation</h2>
    <p>To run this project, you need to install the required libraries. Run the following command in your environment:</p>
    <pre><code>!pip install pandas scikit-learn</code></pre>

    <h2 id="dataset">Dataset</h2>
    <p>The dataset used in this project is the <strong>spam.csv</strong> file, which contains SMS messages labeled as either "spam" or "ham". The dataset is preprocessed to convert labels into binary values (spam = 1, ham = 0).</p>

    <h2 id="steps">Steps</h2>
    <ol>
        <li><strong>Import Libraries:</strong> Import necessary libraries such as pandas, scikit-learn, and others.</li>
        <li><strong>Load the Dataset:</strong> Load the dataset and preprocess it by dropping unnecessary columns and renaming them.</li>
        <li><strong>Split the Data:</strong> Split the dataset into training and testing sets (80% training, 20% testing).</li>
        <li><strong>Convert Text to Features:</strong> Use <code>CountVectorizer</code> to convert text data into numerical features.</li>
        <li><strong>Train the Model:</strong> Train a Naive Bayes classifier using the training data.</li>
        <li><strong>Evaluate the Model:</strong> Evaluate the model's performance using accuracy, confusion matrix, and classification report.</li>
        <li><strong>Test with Custom Input:</strong> Test the model with custom email inputs to classify them as spam or ham.</li>
    </ol>

    <h2 id="results">Results</h2>
    <p>The model achieved an accuracy of <strong>98.39%</strong> on the test set. Below are the evaluation metrics:</p>
    <ul>
        <li><strong>Confusion Matrix:</strong> [[963, 2], [16, 134]]</li>
        <li><strong>Classification Report:</strong>
            <pre>
              precision    recall  f1-score   support

           0       0.98      1.00      0.99       965
           1       0.99      0.89      0.94       150

    accuracy                           0.98      1115
    macro avg       0.98      0.95      0.96      1115
    weighted avg    0.98      0.98      0.98      1115
            </pre>
        </li>
    </ul>

    <h2 id="usage">Usage</h2>
    <p>You can test the model with custom email inputs using the <code>classify_email</code> function. Here's an example:</p>
    <pre><code>
# Test with sample emails
sample_email_1 = "Congratulations! You've won a $1000 Walmart gift card. Click here to claim now."
sample_email_2 = "Hey, can we schedule a meeting for tomorrow at 10 AM?"
print(f"Email: '{sample_email_1}' is classified as: {classify_email(sample_email_1)}")
print(f"Email: '{sample_email_2}' is classified as: {classify_email(sample_email_2)}")
    </code></pre>
    <p>Output:</p>
    <pre><code>
Email: 'Congratulations! You've won a $1000 Walmart gift card. Click here to claim now.' is classified as: Spam
Email: 'Hey, can we schedule a meeting for tomorrow at 10 AM?' is classified as: Ham
    </code></pre>

    <h2>License</h2>
    <p>This project is licensed under the MIT License. See the <a href="LICENSE">LICENSE</a> file for details.</p>

    <h2>Acknowledgments</h2>
    <p>Special thanks to the creators of the <a href="https://www.kaggle.com/uciml/sms-spam-collection-dataset">SMS Spam Collection Dataset</a> for providing the data.</p>
</body>
</html>
