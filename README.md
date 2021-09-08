# Water Polability Project

### Dataset

- [Link](https://www.kaggle.com/adityakadiwal/water-potability) to the dataset

### Libraries used for Data Analysis

- Pandas
- Numpy
- Matplotlib

### Libraries used for Preprocessing 

- SciKit Learn Preprocessing tools

### Classification Models Used

- Logistic Regression
- Linear SVC (Support Vector Classifier)
- Decision Tree Classifier
- Random Forest Classifier
- Linear Support Vector Classifier
- K-Nearest-Neighbor
- Gaussian Naive Bayes
- Gradient Boost (with and without tuning)
- Multi-Layer Perceptron (Artificial Neural Network)
- Extreme Gradient Boosting (XGBoost)
- Light Gradient Boosting Machine (LGBM)
- Categorical Gradient Boosting (CatBoost)

### Data PreProcessing

- Data contains some columns having null values, null values were replaced with mean values `dataframe['col'].mean()`
- Data is scaled using SciKit Learn Standard scaler
- Data is split into 75 to 25, train-test split 
- X axis consisting of all the columns except **Potability**
- Y axis consisting of **Potability**

### Training and Tuning Params

#### Training

- Model Object primarily defined (Sklearn model, except for XGBoost, LGBM and CatBoost)
- Model trained using `model.fit()`
- Training accuracy or score from `model.score()`
- Testing accuracy is calculated from `accuracy_score()` after prediction is made with test data
- Classification report is generated along with Confusion Matrix for the prediction

#### Tuning

- Define Tuning parameters to test over
- Define default model object
- Define cross-validation model for tuning Hyper-parameters using GridSearchCV
- Find best parameters after fitting with training data
- Define model object with computed *best parameters*
- Repeat training process

### Results

| Model                            |  Train   | Test  |
| -------------------------------- | -------- |-------|
| Logistic Regression              |   60.5%  | 62.3% |
| Decision Tree Classifier         |   73.5%  | 64.6% |
| Random Forest Classifier         |   86.6%  | 68.3% |
| Linear Support Vector Classifier |   60.6%  | 62.3% |
| K Nearest Neighbor               |   65.9%  | 66.4% |
| Gaussian Naive Bayes             |   62.8%  | 63.6% |
| Gradient Boosting                |   74.1%  | 66.1% |
| Gradient Boosting (tuned params) |   80.3%  | 67.5% |
| Multi-Layer Perceptron           |   83.5%  | 65.2% |
| Extreme Gradient Boost (tuned)   |   88.8%  | 68.6% |
| Light GBM (tuned)                |   88.6%  | 66.8% |
| Categorical (Cat) Gradient Boost |   89.3%  | 69.1% |

##### Highest test accuracy reached over Categorical Gradient Boost

### Conclusion

The models were primarily trained by droping null cells and replacing null cells with median and mode values for the column. 
Replacing with mean values showed the best results. Highest training and test accuracy is reach by **CatBoost**