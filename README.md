# 🧠 Random Imputation on Categorical and Numerical Columns  
**📄 AI-Generated README (Custom Prompt for Clarity & Learning)**  

---

## 📌 Overview  
This project demonstrates how to handle **missing values** using **Random Imputation** for both **numerical** and **categorical** columns.  
Random imputation fills missing values by sampling existing non-null values from the same column, preserving overall distribution patterns.  

---

## 🧰 Libraries Used  
- pandas  
- numpy  
- matplotlib.pyplot  
- seaborn  
- scikit-learn  

---

## 📂 Datasets Used  
1. **Titanic Dataset** – for numerical missing value handling.  
2. **Housing Dataset** – for categorical missing value handling.  

Both datasets are included in the repository.  

---

## 🧮 Handling Numerical Missing Values  

### Features Used  
- `Age` (with missing values)  
- `Fare`  

### Steps  

1. **Train-Test Split:**  
   Divided data into training and testing subsets.  

2. **Created a New Column:**  
   - Created `Age_Imputed` to store the randomly imputed values for comparison.  

3. **Imputation Process:**  
   - Randomly sampled values from non-null entries in the column.  
   - Filled missing `Age` values in both training and testing data using sampled values.  

4. **Visualization & Analysis:**  
   - **Distribution Plot:** Age before and after imputation had nearly identical shapes, confirming the distribution was preserved. *(Image 1 attached)*  
   - **Variance:** Slightly decreased after imputation.  
   - **Covariance:** Minor change in covariance between `Age` and `Fare`.  
   - **Box Plot:** Outliers remained unchanged. *(Image 2 attached)*  

5. **Key Issue:**  
   Random imputation may assign **different values to identical missing entries** (e.g., two 60-year-olds getting different imputed ages).  
   To fix this, it’s recommended to **store sampled values** for consistent future imputations.  

---

## 🏠 Handling Categorical Missing Values  

### Features Used  
- `FireplaceQu`  
- `GarageQual`  

### Steps  

1. **Train-Test Split:**  
   Split the housing dataset into training and testing data.  

2. **New Columns:**  
   Created `FireplaceQu_Imputed` and `GarageQual_Imputed` for comparison.  

3. **Imputation Process:**  
   - Randomly filled missing categorical values using sampled values from non-null categories in the same column.  

4. **Frequency Check:**  
   - Compared category frequencies **before and after imputation** — the proportions remained almost identical for both features.  

5. **Visualization:**  
   - **Category Distribution (Before):** Frequency of each quality level shown. *(Image 3 attached)*  
   - **Category Distribution (After):** Slight increase in some categories after imputation, but overall proportions preserved. *(Image 5 attached)*  

---

## 📊 Observations  

- **Numerical Columns:**  
  - Random imputation effectively maintained the shape of the data distribution.  
  - Slight reduction in variance and covariance.  

- **Categorical Columns:**  
  - Category balance remained stable.  
  - Frequency graphs confirm minimal distortion after imputation.  

- **Drawback:**  
  - Potential inconsistency when identical missing entries get different random values during multiple imputations.  

---

## 🖼️ Attached Images  

1. **<img width="584" height="433" alt="imp1" src="https://github.com/user-attachments/assets/9d81d796-b959-49db-8548-a3f901d480a2" />
:** Age distribution before vs after imputation  
2. **<img width="543" height="413" alt="imp2" src="https://github.com/user-attachments/assets/8b4878b7-4741-4295-9c19-7a4c6734132d" />
:** Age box plot before vs after  
3. **<img width="567" height="448" alt="imp3" src="https://github.com/user-attachments/assets/c554f49d-492d-4768-9003-0b2a7c8c378a" />
:** Category frequency before imputation (FireplaceQu, GarageQual)  
4. **<img width="567" height="448" alt="imp5" src="https://github.com/user-attachments/assets/985de654-da65-42ba-9b63-60b79eee1600" />
** Category frequency after imputation  

---

📄 *This README was AI-generated using a custom prompt for educational clarity and documentation consistency.*
