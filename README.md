# Medical Insurance Cost Prediction 🏥

A Machine Learning project that predicts individual medical insurance charges based on personal demographics and health metrics. This project demonstrates the end-to-end data science workflow, from Exploratory Data Analysis (EDA) and rigorous Feature Engineering to Model evaluation using **Linear Regression**.

## 🚀 Project Overview

The goal of this project is to build a predictive model that estimates the medical insurance premium (`charges`) for a beneficiary. This helps in understanding the key drivers of insurance costs, such as smoking status, BMI, and age.

## 📊 Key Features & Workflow

### 1. Exploratory Data Analysis (EDA)
* **Distribution Analysis:** Visualized the distribution of numerical features (`age`, `bmi`, `charges`) using histograms and KDE plots.
* **Categorical Analysis:** Count plots for `sex`, `smoker`, and `children`.
* **Correlation Analysis:** Heatmaps to identify relationships between variables (e.g., strong correlation between smoking and charges).
* **Outlier Detection:** Boxplots were used to check for outliers in numerical columns.

### 2. Data Preprocessing & Cleaning
* **Duplicate Removal:** Removed duplicate records to ensure data integrity.
* **Encoding:**
    * **Label Encoding:** Mapped binary columns (`sex`, `smoker`) to 0 and 1.
    * **One-Hot Encoding:** Converted categorical variables (`region`, `bmi_category`) into dummy variables.
* **Scaling:** Applied `StandardScaler` to normalize numerical features (`age`, `bmi`, `children`).

### 3. Feature Engineering & Selection
* **BMI Categorization:** Created a new feature `bmi_category` (Underweight, Normal, Overweight, Obese) to capture non-linear effects of BMI.
* **Statistical Selection:**
    * **Pearson Correlation:** Used to select numerical features with the strongest relationship to the target.
    * **Chi-Square Test:** Used to evaluate the significance of categorical features.

### 4. Model Building
* **Algorithm:** Linear Regression (`sklearn.linear_model.LinearRegression`)
* **Split:** Data split into 80% training and 20% testing sets.

## 📈 Model Evaluation

The model's performance was evaluated using the following metrics:
* **R² Score:** To measure the proportion of variance in the dependent variable explained by the model.
* **Adjusted R²:** To penalize for excessive features and ensure the model generalizes well.

## 🛠️ Tech Stack

* **Language:** Python 3.13.3
* **Libraries:**
    * `pandas` & `numpy` (Data Manipulation)
    * `matplotlib` & `seaborn` (Visualization)
    * `scipy` (Statistical Testing)
    * `scikit-learn` (Modeling & Preprocessing)

## 💻 How to Run

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/insurance-prediction.git](https://github.com/your-username/insurance-prediction.git)
    ```
2.  **Install dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn scipy
    ```
3.  **Run the Notebook:**
    Open `Insurance_Project.ipynb` in Jupyter Notebook or Google Colab.
    *(Note: Ensure `insurance.csv` is in the same directory)*

## 🔮 Future Improvements

* Implement **Logistic Regression** to classify users into risk categories (e.g., High Charge vs. Low Charge).
* Experiment with **Polynomial Regression** to capture non-linear relationships better.
* Deploy the model using **Streamlit** for a user-friendly web interface.

## 👤 Author

**[Lakshay Garg]**
* [GitHub Profile](https://github.com/lakshayy05)
