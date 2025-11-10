Diabetes Prediction Using Support Vector Machine (SVM)

This project focuses on predicting the outcome of diabetes based on various health parameters using a machine learning algorithm—specifically, a Support Vector Machine (SVM). The goal is to classify individuals as either diabetic or non-diabetic based on features such as glucose levels, age, BMI, and other health indicators. The dataset used in this project is the Pima Indians Diabetes Database, which contains information about 768 women with health data related to pregnancy, blood pressure, insulin, BMI, and more.

Key Features of the Dataset

The dataset consists of the following columns:

Pregnancies: Number of pregnancies

Glucose: Plasma glucose concentration (mg/dL)

BloodPressure: Diastolic blood pressure (mm Hg)

SkinThickness: Triceps skinfold thickness (mm)

Insulin: 2-Hour serum insulin (mu U/ml)

BMI: Body mass index (weight in kg / height in m²)

DiabetesPedigreeFunction: Diabetes pedigree function (a function that scores likelihood of diabetes based on family history)

Age: Age of the individual (years)

Outcome: 0 if the individual is not diabetic, 1 if the individual has diabetes

Data Preprocessing

The dataset is first loaded using pandas, and a few initial steps are performed to understand the structure of the data:

Checking for missing values (none in this dataset).

Inspecting basic statistical properties of the features (e.g., mean, standard deviation).

Visualizing data using Seaborn to understand the distribution and correlation between different variables.

Key Insights from Data Exploration:

Glucose and BMI are strongly correlated with the Outcome, which suggests these features are important for predicting diabetes.

The distribution of key variables like Age, Glucose, and BloodPressure is visualized to identify any trends or outliers.

Data Scaling

To prepare the data for modeling, all feature columns (except the target variable Outcome) are standardized using StandardScaler. This step ensures that all features are on the same scale, which is important for algorithms like SVM that are sensitive to the scale of the data.

Machine Learning Model

The project uses the Support Vector Machine (SVM) algorithm, a supervised learning model for classification. SVM works by finding the hyperplane that best separates the data into different classes. In this case, the model classifies individuals as diabetic or non-diabetic based on their health parameters.

Steps in Model Training:

Train-Test Split: The dataset is split into training (75%) and testing (25%) sets.

Model Training: The SVM classifier is trained using the training data with a linear kernel.

Model Evaluation: Accuracy is evaluated on both the training and test sets.

Results:

Training Accuracy: 78.65%

Testing Accuracy: 77.60%

These accuracy scores suggest that the model performs reasonably well in predicting diabetes based on the available features, although there is room for improvement in terms of generalization to unseen data.

Visualization

Several visualizations were created to better understand the dataset:

Heatmap of the correlation matrix shows strong correlations between glucose levels, BMI, and the outcome.

Pairplot to visualize relationships between multiple features.

Regression plots to visualize the relationship between key variables like Glucose and BMI with respect to the outcome.

Conclusion

This project demonstrates the use of machine learning to predict diabetes outcomes based on health data. The Support Vector Machine classifier performed well with an accuracy of approximately 78%, though further tuning of the model or the use of additional features may improve performance.

Future Work

Hyperparameter Tuning: Using techniques like grid search or random search to find the optimal hyperparameters for the SVM model.

Feature Engineering: Exploring additional features or transformations to improve the model's predictive power.

Model Comparison: Comparing SVM with other classification algorithms like Random Forests, Logistic Regression, and Neural Networks to find the best performing model.

Libraries Used:

pandas: Data manipulation and analysis.

seaborn: Data visualization.

sklearn: Machine learning tools, including SVM and data preprocessing.

This project highlights how machine learning techniques can be applied to real-world health data to predict important outcomes, such as diabetes, which can be critical for early diagnosis and intervention.
