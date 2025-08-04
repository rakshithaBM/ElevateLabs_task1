# Internship Task 1 – Data Cleaning & Preprocessing

## 📌 Objective
Clean and preprocess the **Customer Personality Analysis** dataset to prepare it for analysis or modeling.

---

## 📂 Dataset
- **Source**: Customer Personality Analysis (Kaggle)
- **Raw file**: `marketing_campaign.csv`
- **Cleaned file**: `cleaned_marketing_campaign.csv`

---

## 🛠 Tools & Libraries Used
- Python
- Pandas

---

## 🔍 Steps Performed

### 1. Load Dataset
- Loaded `marketing_campaign.csv` into Pandas for processing.

### 2. Handle Missing Values
- Checked for missing values.
- Filled missing values in the **income** column with the median income.

### 3. Remove Duplicates
- Removed duplicate records based on the `id` column.

### 4. Standardize Text Columns
- Formatted `education` and `marital_status` columns to title case and removed extra spaces.

### 5. Convert Date Columns
- Converted `dt_customer` to a standard datetime format.
- Extracted **years_as_customer** from the joining date.

### 6. Feature Engineering
- Created `age` column using `year_birth`.
- Calculated `total_spend` as the sum of spending columns:
  - `mntwines`
  - `mntfruits`
  - `mntmeatproducts`
  - `mntfishproducts`
  - `mntsweetproducts`
  - `mntgoldprods`
- Created `total_accepted_cmp` as the sum of:
  - `acceptedcmp1` to `acceptedcmp5`
  - `response`

### 7. Save Cleaned Dataset
- Exported cleaned data to `cleaned_marketing_campaign.csv`.

---

## 📊 Result
The cleaned dataset contains:
- No missing income values.
- No duplicate records.
- Consistent text formats.
- Useful derived features: `age`, `years_as_customer`, `total_spend`, `total_accepted_cmp`.

---

## 📎 Files in Repository
- `marketing_campaign.csv` → Raw dataset.
- `cleaned_marketing_campaign.csv` → Cleaned dataset.
- `task1_cleaning.py` → Python cleaning script.
- `README.md` → Documentation of steps.

---

## 🚀 How to Run
1. Place the raw dataset in the same folder as `task1_cleaning.py`.
2. Run:
   ```bash
   python task1_cleaning.py
