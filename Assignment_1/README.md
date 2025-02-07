### **Recursive Feature Elimination with Linear Regression**
**1. Import Necessary Libraries**

•	NumPy & Pandas – For data manipulation.

•	Matplotlib – For visualization.

•	Scikit-learn Modules – For dataset loading, model training, evaluation, and feature selection.

**2. Load & Explore the Diabetes Dataset**

•	Loads the Diabetes dataset from Scikit-learn.

•	X contains features (age, BMI, blood pressure, etc.).

•	y is the target variable (disease progression).

•	The dataset is converted into a DataFrame for easy inspection.

![image](https://github.com/user-attachments/assets/9ec15ed6-215d-4130-b531-f121fab0b036)

**3. Split Dataset into Training and Testing Sets**

•	Splits data into 80% training and 20% testing for model evaluation.

•	random_state=42 ensures results remain consistent.

**4. Train a Baseline Linear Regression Model**

•	A basic linear regression model is trained using all features.

•	The R² score is computed to measure model performance on the test set.

![image](https://github.com/user-attachments/assets/5e4a9f57-cd81-4603-859a-ebff5c0ad7ad)

**5. Apply Recursive Feature Elimination (RFE)**

•	RFE is applied iteratively, starting with all 10 features and progressively removing the least important one until only one remains.

•	After each iteration, the model’s performance is evaluated using the R² score.

•	The R² score is stored for visualization.

**6. Plot R² Score vs. Number of Features**

•	A line plot is created to visualize the effect of feature elimination on model performance.

•	Helps in determining the optimal number of features.

![image](https://github.com/user-attachments/assets/fb6858b5-2b44-487d-882a-dabd8cc97926)

**7. Find the Best Number of Features**

•	Finds the optimal number of features that maximizes the R² score.

 ![image](https://github.com/user-attachments/assets/2dcf51ed-b6de-460a-91d3-7ff894597fec)

**8. Analyze Feature Importance**

•	Runs RFE one last time, selecting only one most important feature.

•	Creates a table ranking all features based on importance.

•	The most important features have a rank of 1.

 ![image](https://github.com/user-attachments/assets/556b54b8-9402-4085-9bd5-41a57e8eb131)
 
![image](https://github.com/user-attachments/assets/5374403c-0f20-4156-bb7d-2d8b29940671)

![image](https://github.com/user-attachments/assets/59f257ab-e8ce-4fc7-a37c-188945836e2d)

![image](https://github.com/user-attachments/assets/39980e81-fb45-423a-a5bb-214deb324349)

![image](https://github.com/user-attachments/assets/6399834d-7620-43c5-8b05-55e924c59f50)

#### **REFLECTIONS:**

**1.	What did you learn about feature selection using RFE?**

Recursive Feature Elimination (RFE) systematically removes less important features to improve model performance and interpretability. It helps in identifying the most influential variables, reducing overfitting and improving model generalization.

**2.	How does RFE compare to other feature selection methods like LASSO in terms of methodology and results?**

Unlike LASSO, which applies L1 regularization to shrink coefficients to zero, RFE iteratively removes the weakest features based on model performance. 

**3.	What insights can you draw about the dataset from the selected features?**

The most important features identified by RFE suggest which factors have the strongest influence on diabetes progression. For example, if BMI or blood pressure ranks highly, it reinforces their known medical significance.
