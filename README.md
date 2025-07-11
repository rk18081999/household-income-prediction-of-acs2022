# 🏡 Predicting Household Income Using Machine Learning  
**Exploring Socioeconomic and Housing Dynamics with ACS 2022 PUMS Data**

## 📊 Overview
This project applies machine learning to predict household income levels using socioeconomic, housing, and employment-related variables. The dataset originates from the **American Community Survey (ACS) 2022 Public Use Microdata Sample (PUMS)** and includes 819,000+ records from 26 U.S. states.

### 🔍 Research Question  
**Can we predict a household's income category based on demographic, housing, and employment characteristics?**

## 🧠 Objectives
- Analyze relationships between household income and factors like housing unit type, property value, and employment.
- Build ML models to predict income categories.
- Evaluate model performance and deploy a robust predictive solution.

## 📁 Dataset  
- **Source**: ACS 2022 PUMS Data  
- **Size**: 819,228 records | 241 features  
- **Filtered**: Focus on 26 states with >50,000 records each  
- **Key Variables**:  
  - *Demographic*: Age, Sex, Race, Marital Status  
  - *Economic*: Household Income (HINCP), Employment, Personal Income  
  - *Housing*: Property Value (VALP), Monthly Rent (GRNTP), Tenure (TEN), Unit Type

## 🧹 Data Preprocessing
- **Imputation**: Median-based for numeric columns (e.g., NPF, OCPIP)  
- **Outlier Removal**: IQR-based filtering for HINCP and other skewed metrics  
- **Feature Engineering**:
  - Income category bins (Very Low → Very High)
  - New variables: `Family_Type`, `TEN`  
- **Encoding & Standardization**: One-hot encoding + numerical scaling

## 📈 Feature Selection
- **LDA**: Used for dimensionality reduction & category separation visualization  
- **Random Forest**: Top predictors ranked (e.g., OCPIP, SMOCP, VALP)

## 🤖 Models Trained
| Model            | Accuracy | Notes |
|------------------|----------|-------|
| Random Forest    | ~91%     | Interpretable, fast training |
| XGBoost          | ~93%     | Best performance overall |
| Neural Network   | ~93%     | TensorFlow + Keras, higher complexity |
| **Ensemble Model** | **93.19%** | Combines all 3 models for best generalization |

## ✅ Preferred Model: XGBoost
- Highest accuracy (93.21%)
- Faster and more interpretable than NN
- Scalable and easy to deploy

## 📦 Tech Stack
- **Python**, **Scikit-learn**, **XGBoost**, **Keras**, **TensorFlow**
- **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**
- **Jupyter Notebooks**, Git, GitHub LFS (for large data)

## 📌 Repository Structure
```
📦household-income-prediction/
 ┣ 📁data/                # ACS PUMS subset (via Git LFS)
 ┣ 📁notebooks/           # EDA, preprocessing, model training
 ┣ 📁models/              # Trained models (optional)
 ┣ 📄README.md
 ┣ 📄requirements.txt     # All libraries & versions used
 ┗ 📄final_report.pdf     # Project summary / slides
```

## 🧠 Authors  
- **Rahul Kanth Panganamamula**  
- **Minjae Lee**  
- **Mahanth Dasari**

## 🏁 Conclusion  
This project demonstrates the effectiveness of ensemble ML models in analyzing and predicting socioeconomic patterns from large-scale public data. Insights can inform public policy, housing affordability studies, and economic development programs.
