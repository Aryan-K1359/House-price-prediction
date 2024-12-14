Report: Predicting  Housing Prices Using XGBoost

---

Project Overview:

The goal of this project is to predict housing prices  using a Housing Dataset. The dataset consists of multiple features such as median income, house age, and latitude/longitude, which are used to predict the median house value (price) in a district. The machine learning model chosen for this project is the XGBoost Regressor, a powerful model that excels in predictive tasks and is known for its performance and efficiency.

---

Data Overview:

The dataset is loaded from sklearn.datasets.fetch_housing() , which provides a regression dataset with the following features:

- MedInc - Median income in block group.
- HouseAge - Median house age in block group.
- AveRooms - Average number of rooms per household.
- AveOccup - Average number of household members.
- Lat - Latitude of block group.
- Lon - Longitude of block group.
- MedHouseVal (Price) - Target variable (Median house value for various districts).

---

Exploratory Data Analysis (EDA):

Before building the model, we perform exploratory data analysis (EDA) to understand the relationships between the features and the target variable.

- Correlation Matrix:
   A correlation matrix was constructed to understand the linear relationships between different features and the target variable. We used a heatmap for better visualization of the correlations.



- Features and Target Variables:
   We separated the features and target variable:
   - X contains all features except the target variable (price).
   - Y contains the target variable (price).

---

Data Preprocessing:

1. Train-Test Split:
   The data was split into training and testing sets using an 80-20 split. The training set was used to train the model, while the testing set was used to evaluate its performance.
   


2. **Model Initialization:** 
   The **XGBoost Regressor** model was selected for this task due to its robustness and efficiency for regression problems.
   


3. Model Training:
   The model was trained on the training data (X_train, Y_train).



---

Model Evaluation:

Once the model was trained, predictions were made on both the training and testing datasets. The following performance metrics were calculated:

1. **Training Data:**
   - **R-Squared Error (Training):** Measures the proportion of variance in the dependent variable that is predictable from the independent variables.
   

   - Mean Absolute Error (Training): Measures the average magnitude of the errors in a set of predictions, without considering their direction.
   


   - Results:
     - R-Squared Error (Training): 0.945
     - Mean Absolute Error (Training): 0.192

   The high R-Squared score indicates that the model fits the training data well.

2. Testing Data:
   - R-Squared Error (Testing): Evaluates how well the model generalizes to unseen data.
   - Mean Absolute Error (Testing): Indicates the average prediction error for the test set.



   - Results:
     - R-Squared Error (Testing): 0.841
     - Mean Absolute Error (Testing): 0.308

   The model performs well on the testing data, though there is a slight reduction in performance compared to the training set. This is expected due to the model’s tendency to overfit on the training set.

---

Visualization:

To better understand the model's performance, we visualized the actual vs predicted prices on the training data:

The scatter plot shows that the predicted prices are quite close to the actual prices, indicating a good fit for the model.

---

Conclusion:

- The XGBoost Regressor performed well in predicting housing prices with an R-squared value of 0.945 on the training data and 0.841 on the test data.
- The Mean Absolute Error was 0.192 for the training data and 0.308 for the testing data, which indicates the model’s good performance in terms of prediction accuracy.
- Further improvements could include parameter tuning, cross-validation, and exploring different machine learning models for comparison.

This project demonstrated the ability of machine learning models, particularly XGBoost, to predict complex real-world data such as housing prices, with promising results.
