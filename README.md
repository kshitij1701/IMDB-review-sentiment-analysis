Dataset used : 
I have used the “IMDB reviews” dataset from kaggle for the task of sentiment analysis.
![Screenshot 2023-11-28 191005](https://github.com/kshitij1701/IMDB-review-sentiment-analysis/assets/152283665/1bf7d5fa-1ce4-414e-a05b-b3c53ea97293)

The dataset has 50,000 rows.

Data Pre-processing:

For data preprocessing, I begin by loading the dataset from the provided CSV file. I transform the 'sentiment' column into numerical values, mapping 'positive' to 1 and 'negative' to 0.

![Screenshot 2023-11-28 191119](https://github.com/kshitij1701/IMDB-review-sentiment-analysis/assets/152283665/efa4ebd7-5193-43dc-b408-d103193124d8)

To ensure proper training, I split the data into training, validation, and test sets using the train_test_split function.

![Screenshot 2023-11-28 191138](https://github.com/kshitij1701/IMDB-review-sentiment-analysis/assets/152283665/6c0e8d04-7a45-4d27-ac3d-95a138a12724)

Next, I tokenize and pad the text sequences using TensorFlow's Tokenizer and pad_sequences functions, ensuring consistent sequence lengths for input.

![Screenshot 2023-11-28 191151](https://github.com/kshitij1701/IMDB-review-sentiment-analysis/assets/152283665/db1bbd88-855e-4e55-95a3-976c98dd05f7)

Model Architecture:

When creating the model structure, I use TensorFlow's Keras API. 
Embedding Layer: This layer helps the model understand the meaning of words.
MultiHeadAttention Layer: This layer looks at different parts of the text at the same time to capture context.
GlobalAveragePooling1D Layer: This layer combines all the information gathered to create a summary of the text.
Dense Layers: These are simple layers that do additional processing.
Sigmoid Activation: This is like a switch that helps the model make a decision - it's set up for binary choices like positive or negative.

![Screenshot 2023-11-28 191313](https://github.com/kshitij1701/IMDB-review-sentiment-analysis/assets/152283665/e08b88b6-0c18-4275-a2f2-4dc254e90290)

![Screenshot 2023-11-28 191332](https://github.com/kshitij1701/IMDB-review-sentiment-analysis/assets/152283665/a1c739fa-a9b9-4775-b112-118e4157ea2c)

Defining the hyperparameters for transformer model:

![Screenshot 2023-11-28 191345](https://github.com/kshitij1701/IMDB-review-sentiment-analysis/assets/152283665/603b2b7c-0fb6-4702-92b9-5d19caca0d11)

Initializing the model and starting the training process:

![Screenshot 2023-11-28 191400](https://github.com/kshitij1701/IMDB-review-sentiment-analysis/assets/152283665/93b3631c-5e51-41d2-bb86-fc750b321d5d)

Model Evaluation:

I evaluated the model on the test set to check its generalization performance. I compute various metrics, including accuracy, precision, recall, F1-score, and a confusion matrix. 
![Screenshot 2023-11-28 191420](https://github.com/kshitij1701/IMDB-review-sentiment-analysis/assets/152283665/cc7801b8-e16c-4b82-b6b5-42d7709b2e59)

Accuracy provides an overall measure of correct predictions, while precision and recall offer insights into the model's ability to identify positive instances accurately and capture all positive instances, respectively. 
F1-score provides a balanced measure between precision and recall. 
The confusion matrix breaks down true positive, true negative, false positive, and false negative predictions in detail.

The model has an overall accuracy of 86%.


Testing the model on some reviews:

![Screenshot 2023-11-28 191436](https://github.com/kshitij1701/IMDB-review-sentiment-analysis/assets/152283665/b721f4e7-5538-437e-b250-ba4e8786e13a)

![Screenshot 2023-11-28 191448](https://github.com/kshitij1701/IMDB-review-sentiment-analysis/assets/152283665/55fed3d5-7bc9-4eb3-a4ff-fb5da8d31b8c)





