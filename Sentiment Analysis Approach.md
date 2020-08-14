# Our Approach

## About the Data
<img width="500" alt="image" src=https://user-images.githubusercontent.com/48685014/90114315-220eb700-dd85-11ea-9cc4-d93df9f97b71.png>

There are 3 columns in the data frame, namely review_id, review and rating. The variable review_id is the unique identifier for the data, review is the text data from users in string and rating is the categorical data of the users' sentiments. The predictor variable is the review text, while the 5 different classes of reviews serves as the response variable.

## Train-Test Split
The data frame is splitted randomly with scikit-learn train-test split library, with 20% test set and 80% training set.

## Data Pre-processing
The data is pre-processed as there is a need to convert the text data into numerical data for the model to train. Hence, we apply Count Vectorizer and Term frequency – Inverse document frequency (Tf-Idf) Transformer on the text data through a pipeline, fulfilled by scikit-learn libraries. Count Vectorizer converts the text data into a bag of words where the words are represented by how many times it appears in the corpus. Tf-Idf Transformer, on the other hand, reduces the impact of the words that occur very frequently in the corpus.

## Model Training
The processed data is then passed to the logistic regression classifier to train on the training set. However, the other statistical models were also experimented on the training set to evaluate the performance, but these models fare poorly than logistic regression in terms of the classification accuracy of the test set.

<img width="370" alt="image" src=https://user-images.githubusercontent.com/48685014/90265270-ea873400-de84-11ea-9a14-63c67c3e79ae.png>
<img width="500" alt="image" src=https://user-images.githubusercontent.com/48685014/90265531-494cad80-de85-11ea-8db9-b2c67dc7f327.png>

## Submission
Finally, with the trained model we can test it on the test data frame and make the final submission.
