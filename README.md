# Census Income Prediction

This project analyzes a census-income dataset to predict whether an individual's annual income exceeds $50,000. It includes data cleaning, exploratory data analysis (EDA), and machine learning model building.

## Dataset

The dataset used in this project is `census-income .csv`, which contains information about individuals, including:

-   `age`: The age of the individual.
-   `workclass`: The type of employment.
-   `education`: The highest level of education achieved.
-   `education-num`: The numerical representation of the education level.
-   `marital-status`: The marital status of the individual.
-   `occupation`: The individual's occupation.
-   `relationship`: The relationship status of the individual.
-   `race`: The individual's racial background.
-   `sex`: The gender of the individual.
-   `capital-gain`: Capital gains.
-   `capital-loss`: Capital losses.
-   `hours-per-week`: The number of hours worked per week.
-   `native-country`: The individual's country of origin.
-   `annual_income`: The target variable, indicating if the annual income is `>50K` or `<=50K`.

## Analysis and Methodology

The project follows a structured approach to data analysis and modeling:

### 1. Data Cleaning and Preprocessing

-   **Duplicate Removal**: Identical rows were removed from the dataset to ensure data integrity.
-   **Outlier Treatment**: Outliers in numerical features (`age`, `fnlwgt`, `education-num`, `capital-gain`, `capital-loss`, and `hours-per-week`) were handled using the Interquartile Range (IQR) method.
-   **Categorical Encoding**: All categorical columns were converted to numerical format using `LabelEncoder`.

### 2. Exploratory Data Analysis (EDA)

-   Box plots were used to visualize the distribution of categorical features.
-   <img width="707" height="547" alt="image" src="https://github.com/user-attachments/assets/199ea235-ab13-43b5-8bc0-e6e637374a85" />
<img width="931" height="548" alt="image" src="https://github.com/user-attachments/assets/9ec4c2fb-5100-4111-b59c-ad9094da9584" />




### 3. Feature Engineering and Selection

-   **Multicollinearity Check**: The Variance Inflation Factor (VIF) was used to identify and handle multicollinearity among the features. Highly correlated features like `hours-per-week`, `education-num`, `race`, and `native-country` were identified and removed in a step-by-step process.

### 4. Machine Learning Models

-   **Logistic Regression**: A logistic regression model was built to predict the `annual_income` target variable. The model achieved an accuracy of approximately **81.87%** on the test data.
-   **Linear Regression**: A linear regression model was developed to predict `hours-per-week` using `age`, `fnlwgt`, `education-num`, `capital-gain`, and `capital-loss` as features. This model resulted in a perfect fit, indicated by an R-squared ($R^2$) value of 1.00. This suggests that after outlier removal, the `hours-per-week` column has a constant value across the dataset.

## How to Run the Project

1.  Clone this repository.
2.  Ensure you have Python and the required libraries installed.
    ```
    pip install pandas numpy scikit-learn matplotlib seaborn statsmodels
    ```
3.  Open the `ratan_pratap_singh.ipynb` Jupyter Notebook.
4.  Run all the cells in the notebook to reproduce the analysis and model results.
colab link:https://colab.research.google.com/drive/1Ho2d1D9DELysmv0BX_sUJNGsKU8HwG9W?usp=sharing
