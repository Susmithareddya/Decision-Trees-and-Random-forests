### Decision Trees and Random Forest for Song Popularity Prediction

This repository demonstrates the implementation of decision trees and a custom random forest model to predict song popularity. The project involves training models on a dataset of songs, assessing their popularity, and comparing the performance of a custom random forest implementation with scikit-learn's RandomForestClassifier.

---

#### Features

1. **Bootstrap Sampling**: Implementation of a function to create bootstrap samples from the training dataset.
2. **Custom Random Forest Algorithm**:
   - Uses `DecisionTreeClassifier` from scikit-learn for individual trees.
   - Implements key components like feature selection and aggregation using SciPy and NumPy.
3. **Evaluation**:
   - Calculates accuracy of the custom model.
   - Compares it with the performance of scikit-learn's RandomForestClassifier.

---

#### Dataset
- **Train Data**: `train-songs.csv` contains features and labels for training the model.
- **Test Data**: `test-songs.csv` is used to evaluate the model's accuracy.

---

#### Workflow

1. **Bootstrap Sampling**:
   - A function generates a bootstrap sample of size `N` from the training dataset, enabling robust training of decision trees.

2. **Custom Random Forest Implementation**:
   - The `RandomForest` class is defined with parameters for the number of trees, maximum features per tree, bootstrap sample size, minimum node size, and maximum depth.
   - Individual trees are trained using `DecisionTreeClassifier`.
   - Final predictions are made by aggregating the predictions of all trees using majority voting.

3. **Training and Testing**:
   - The custom random forest model is trained on the training dataset with specified parameters.
   - Accuracy is calculated on the test dataset.

4. **Comparison with scikit-learn's RandomForestClassifier**:
   - The same dataset is used to train and evaluate scikit-learn's implementation for comparison.

---

#### Results
- **Custom Random Forest Accuracy**: 79.95%
- **scikit-learn Random Forest Accuracy**: 80.6%

The results indicate that the custom implementation closely matches the performance of scikit-learn's optimized library.

---

#### Setup Instructions

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install required libraries:
   ```bash
   pip install numpy pandas scikit-learn scipy
   ```

3. Place the `train-songs.csv` and `test-songs.csv` files in the project directory.

4. Run the script:
   ```bash
   python song_popularity_prediction.py
   ```

---

#### Custom Random Forest Parameters

| Parameter            | Value |
|----------------------|-------|
| Number of trees      | 100   |
| Maximum features     | 2     |
| Bootstrap sample size| 20000 |
| Minimum node size    | 1     |
| Maximum tree depth   | 10    |

---

#### Contributions

Feel free to fork this repository and contribute by improving the custom random forest implementation or adding more features.

---

#### Disclaimer
This project is intended for educational purposes to demonstrate the inner workings of random forest algorithms.
