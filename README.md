# CISData Preparation Pipeline
1. Original Data Source
The dataset used in this project is from the ADBench repository, which provides benchmark datasets for anomaly detection.
Dataset: Credit Card Fraud Dataset
Source: https://github.com/Minqi824/ADBench/tree/main/adbench/datasets

2. Data Acquisition
We downloaded the credit card fraud dataset from the ADBench repository.
The dataset contains labeled instances of credit card transactions, with labels indicating whether a transaction is fraudulent or not.

3. Data Preprocessing
The following preprocessing steps were applied to the dataset:
Feature Scaling: To ensure all features were on a similar scale, numerical features were normalized. This step helps prevent features with larger ranges from dominating the model training process.
Train-Test Split: The dataset was split into training and testing subsets using an 80/20 split. The training set was used to fit the model, while the testing set was used to evaluate the model's performance.
Training Data: 80% of the original dataset
Testing Data: 20% of the original dataset
This was done using the train_test_split function from scikit-learn.

4. Data Transformation
The data was stored in a NumPy array format and saved as .npz files, which were then used as input for the DeepSVDD model. This format ensures compatibility with the DeepOD library and allows for efficient data handling during model training.

5. Final Dataset
After preprocessing, the final dataset was ready for model training and evaluation. It consisted of:
Training Set: 80% of the dataset, used to train the DeepSVDD model.
Test Set: 20% of the dataset, used to evaluate the performance of the model.
