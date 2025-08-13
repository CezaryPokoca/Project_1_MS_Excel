# UFC Fights – Data Analysis Project

## 📄 Project Overview

This project is a data analysis case study performed in **Microsoft Excel** for portfolio purposes. The dataset contains detailed information on UFC fights, fighters, and event locations.
The objective was to clean, merge, and analyze the data to answer client-specific questions and extract actionable insights.

---

## 📂 Spreadsheet Structure

* **Yellow Sheets** – Raw Data
* **Red Sheets** – Client Questions
* **Green Sheets** – Analysis & Answers

---

## 🛠 Data Cleaning and Preparation

The following steps were performed to prepare the dataset for analysis:

| Step | Action                       | Description                                                                              |
| ---- | ---------------------------- | ---------------------------------------------------------------------------------------- |
| 1    | **Data Consolidation**       | Merged data from `ufc_fights`, `ufc_fighters`, and `ufc_location` into a single dataset. |
| 2    | **Formatting Verification**  | Standardized date, numeric, and text formats across all sheets.                          |
| 3    | **Data Reduction**           | Removed unnecessary and duplicate columns to streamline the dataset.                     |
| 4    | **Weight Conversion**        | Converted fighter weight from pounds (**lbs**) to kilograms (**kg**).                    |
| 5    | **Height Conversion**        | Converted fighter height from feet and inches to centimeters (**cm**).                   |
| 6    | **Age Calculation**          | Created `age` column from fighter’s birth date and fight date.                           |
| 7    | **Category Standardization** | Unified and renamed weight class categories for consistency.                             |
| 8    | **Final Dataset Creation**   | Generated `UFC_final_data` sheet containing cleaned, formatted data ready for analysis.  |

---

## 📊 Analysis & Findings

* Used pivot tables, conditional formatting, and aggregation functions to answer client-specific questions.
* Identified patterns in fighter performance across different weight classes.
* Examined correlations between fighter age, height, weight, and fight outcomes.
* Analyzed geographical distribution of UFC events based on location data.

### 🔍 Additional Insights

#### Analyze\_Q6 – Correlation and Regression Analysis

**Summary:**
This analysis examines the relationship between significant strikes landed (`sig_str_winner`) and the distribution of those strikes to different target areas — head (`head_winner`), body (`body_winner`), and legs (`leg_winner`).

* Head strikes show the strongest positive correlation with total significant strikes landed (r = 0.854).
* Body strikes have a weak relationship (r ≈ 0.14), and leg strikes show negligible correlation.

A simple linear regression using `head_winner` as the independent variable produced:

* Multiple R = 0.854
* R² = 0.7298
* Standard Error = 0.082
* p-value ≈ 0 (statistically significant)

**Conclusions:**

* Head strikes alone explain \~73% of the variance in total significant strikes landed.
* Body and leg strikes contribute minimally to predicting total significant strikes.
* Head strikes play a dominant role in defining a fighter’s striking success within a bout.

---

#### Analyze\_Q7 – t-Test Analysis

**Summary:**
This analysis compares two groups of fights:

1. KO/TKO or Submission victories (`KO_TKO_submission`)
2. Normal decision fights (`normal_fights`)

A two-sample t-test (unequal variances) was conducted, yielding:

* Mean (KO/TKO/Submission): 0.5683
* Mean (Normal Fights): 0.1643
* t Stat = 25.632
* p-value ≈ 8.21 × 10⁻¹³⁶
* Cohen’s d = 0.707 (large effect size)

**Conclusions:**

* KO/TKO or Submission fights have significantly higher mean values for the measured variable than decision fights.
* The difference is highly statistically significant and practically meaningful.
* The measured variable likely has a decisive role in early finishes compared to decisions.

---

## ✅ Summary & Conclusions

* **Clean Data is Key** – Removing inconsistencies and standardizing formats made the dataset more reliable and easier to analyze.
* **Feature Engineering Added Value** – Calculated columns (age, metric conversions) provided deeper analytical possibilities.
* **Client Questions Fully Addressed** – Clear, data-backed answers supported by visualizations met all client requirements.
* **Key Insights Highlighted** – Head strikes dominate striking success, and certain performance indicators strongly influence fight outcomes.

---

## 📎 Files in Repository

* `ufc_fights_final.xlsx` – Complete project file with all sheets (data, questions, analysis, results).
* `README.md` – Project description and methodology (this file).

---

## 💡 Tools Used

* **Microsoft Excel** – Data cleaning, transformation, and analysis.

---

