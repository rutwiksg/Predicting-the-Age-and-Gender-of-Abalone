# Predicting-the-Age-and-Gender-of-Abalone

#### 1. **Introduction**
Abalones are edible mollusks, and predicting their age and gender is important for various scientific and commercial purposes. Traditionally, age is determined by counting rings on the shell, a labor-intensive process. This project aims to build models to predict age using measurable attributes and to classify gender using machine learning techniques.

#### 2. **Data Overview**
The dataset includes attributes such as gender (M, F), length, diameter, height, whole weight, shucked weight, viscera weight, shell weight, and rings (which determine age). These features are a mix of continuous and nominal data.

#### 3. **Age Prediction Model**
- **Approach:** A regression model was built to predict age using various continuous features.
- **Key Findings:**
  - Features like diameter, height, and various weight measures were significant predictors of age (p-value < 0.05).
  - The model’s **Adjusted R-squared** was 0.3855, indicating that 38.55% of the variation in age is explained by the predictors.
  - The model’s **RMSE** was 2.29 and **MAPE** was 14.3%, reflecting moderate accuracy.
  - Residual analysis showed a normal distribution, with no patterns suggesting a decent model fit.
  
#### 4. **Gender Prediction**
- **Approach:** Logistic regression and linear discriminant analysis (LDA) were applied to classify gender.
- **Performance:** 
  - The **AUC** for logistic regression was 0.55, only slightly better than random guessing (AUC = 0.5).
  - The high false positive rate indicated the models were poor at distinguishing between male and female abalones.

#### 5. **Dimension Reduction**
- **Principal Component Analysis (PCA)** and **Exploratory Factor Analysis (EFA)** were applied to reduce dimensionality.
- Neither method improved the model's performance, with AUCs of 50.9% and 50.1%, respectively, suggesting dimension reduction techniques did not benefit this dataset.

#### 6. **Conclusion**
The regression model provides moderate accuracy for predicting abalone age, but predicting gender using the available features was largely unsuccessful. Dimension reduction techniques failed to improve classification models, likely due to the nature of the dataset. Further refinement or additional features may be needed to enhance model performance.
