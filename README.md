# Water Polability Project

## Kaggle Dataset

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


#### Preliminary training results without model tuning

##### Accuracy Scores
 
| Model                            |  Train   | Test  |
| -------------------------------- | -------- |-------|
| Logistic Regression              |   60.9%  | 61.3% |
| Linear Support Vector Classifier |   61.1%  | 61.9% |
| Random Forest Classifier         |   100%   | 65.7% |

Previous accuracy scores were produced due to not using a Scaler and using Median to replace null values and used a 75-25 split.

##### Trial with replacing null values with column means and using Standard Scaler with a 75-25 split

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

#### Highest test accuracy reached over Random Forest Classifier