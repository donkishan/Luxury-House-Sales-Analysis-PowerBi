# 📘 README — Luxury Housing Bangalore Data Cleaning & Processing Pipeline

## 📌 Project Overview
This project performs end-to-end data cleaning, feature engineering, validation, and export for the *Luxury Housing Bangalore* dataset.  
It converts raw real-estate data into a clean, analysis-ready dataset with fully derived metrics such as:

- **price_inr** (converted from crores → INR)
- **price_per_sqft**
- **price_per_sqft_lakh**
- **Quarter & Year extraction**
- **Booking flag**
- **Cleaned unit size**
- **Imputed values for missing fields**

The final cleaned dataset is saved as:

```
Cleaned_Luxury_Housing_Bangalore_final.csv
```

---

## 📁 Project Structure

```
data/
│── Luxury_Housing_Bangalore.csv              
│── Cleaned_Luxury_Housing_Bangalore_final.csv
notebooks/
│── cleaning_pipeline.ipynb                   
                    
README.md
```

---

## 🧹 Key Cleaning Steps

### ✔ 1. Loading & Initial Inspection
- Check null values  
- Data types  
- Summary statistics  

### ✔ 2. Cleaning Ticket Price
- Remove `₹`, commas, `Cr`, alphabets  
- Convert to float  
- Convert Crores → INR  

### ✔ 3. Cleaning Unit Size
- Convert text → numeric  
- Replace **-1** with median  
- Ensure no zero / negative areas  

### ✔ 4. Derived Metrics
| Column | Description |
|--------|-------------|
| price_inr | Price in INR |
| price_per_sqft | INR per sqft |
| price_per_sqft_lakh | Lakhs per sqft |
| quarter_number | Extracted quarter |
| purchase_year | Extracted year |
| booking_flag | 1 = booked, 0 = future |

### ✔ 5. Date Parsing & Imputation
- Convert to datetime  
- Extract quarter and year  
- Fill missing values (median or defaults)  

---

## 📊 Outputs
Final cleaned dataset contains:
- All original columns  
- Fully cleaned numeric values  
- Derived features for price and time analysis  

---

## 🧠 Technologies Used
- Python  
- Pandas  
- NumPy  
- Regex  
- SQLAlchemy  
- Jupyter Notebook  

---

## 🚀 How to Use

### Clone
```
git clone <repo-url>
```

### Install dependencies
```
pip install -r requirements.txt
```

### Run Jupyter Notebook
```
jupyter notebook
```


```

---

## 🙌 Author
Kishan H S  

