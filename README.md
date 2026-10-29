# 🏥 Hospital Readmission & Patient Flow Analytics

An end-to-end healthcare analytics project that uses **Python, SQL, and Power BI** to analyze hospital readmissions, patient flow, length of stay, treatment costs, and patient risk factors.

The project transforms hospital encounter data into actionable insights that can help healthcare teams understand readmission patterns, monitor operational performance, and support data-driven decisions.

## 📌 Project Overview

Hospital readmissions can increase healthcare costs and create additional pressure on hospital resources. This project analyzes patient encounters to identify patterns associated with readmissions and understand how patient characteristics, diagnoses, length of stay, and treatment costs relate to hospital operations.

The project covers the complete analytics workflow, from data generation and exploratory analysis to SQL-based business analysis and Power BI reporting.

**Hospital Context:** Shanti Multispecialty Hospital, Gurugram
**Reporting Period:** Financial Year 2024–25

> **Note:** The datasets in this project are synthetically generated for analytics and portfolio demonstration purposes. They do not represent actual hospital records or real patient outcomes.

## 🎯 Project Objectives

* Analyze the overall 30-day hospital readmission rate.
* Identify diagnosis categories associated with higher readmission rates.
* Examine readmission patterns across different age groups.
* Analyze the relationship between length of stay and hospital costs.
* Study medication counts, comorbidities, and previous admissions.
* Identify frequent hospital users and evaluate their cost contribution.
* Build a feature-engineered dataset for Power BI visualization.
* Translate healthcare data into meaningful business insights.

## 🛠️ Technology Stack

| Technology   | Purpose                                                      |
| ------------ | ------------------------------------------------------------ |
| Python       | Data generation, cleaning, feature engineering, and analysis |
| Pandas       | Data manipulation and preprocessing                          |
| NumPy        | Numerical operations and calculations                        |
| Matplotlib   | Data visualization                                           |
| Seaborn      | Statistical visualizations                                   |
| SQL          | Data modeling, joins, aggregations, and business analysis    |
| Power BI     | Interactive dashboards and reporting                         |
| CSV          | Data storage and exchange                                    |
| Git & GitHub | Version control and project hosting                          |

## 📂 Project Structure

```text
Hospital_Readmission_Patient_Flow_Analytics/
│
├── 01_create_tables.sql
├── 02_business_questions.sql
│
├── generate_data.py
├── eda.py
│
├── patients.csv
├── doctors.csv
├── encounters.csv
├── encounters_features_powerbi.csv
│
└── hospital-readmission-patient-flow-analytics (1).pbix
```

## 📊 Dataset Description

The project contains three primary datasets and one feature-engineered dataset.

| Dataset                           | Records | Description                                                                       |
| --------------------------------- | ------: | --------------------------------------------------------------------------------- |
| `patients.csv`                    |   7,500 | Patient demographics, age, location, and insurance type                           |
| `doctors.csv`                     |      39 | Doctor details, departments, designations, and experience                         |
| `encounters.csv`                  |   9,093 | Hospital encounters, diagnoses, length of stay, costs, and readmission indicators |
| `encounters_features_powerbi.csv` |   9,093 | Feature-engineered encounter data prepared for Power BI                           |

### Key Features

* Patient and encounter identifiers
* Age and demographic information
* Department and diagnosis category
* Admission and discharge dates
* Length of stay
* Comorbidity count
* Number of medications and procedures
* Total hospital bill and out-of-pocket expenses
* Readmission indicators
* Age and length-of-stay categories
* Previous admissions within 365 days
* Frequent-flyer classification

## 🔍 SQL Business Analysis

The SQL scripts establish the database structure and analyze healthcare operations through business-focused queries.

Key analytical areas include:

1. **30-Day Readmission Rate:** Measure readmissions by diagnosis category.
2. **Age-Based Risk Segmentation:** Compare readmission patterns across age groups.
3. **Length of Stay Analysis:** Examine readmission rates and costs across stay-duration groups.
4. **Medication Analysis:** Explore medication counts and readmission patterns.
5. **Previous Admissions:** Evaluate prior hospital visits within a 365-day window.
6. **Frequent-Flyer Analysis:** Identify patients with repeated encounters.
7. **Cost Analysis:** Investigate hospital bills and patient out-of-pocket expenses.
8. **Risk Analysis:** Develop and examine patient risk-related features.

These analyses support operational monitoring and help identify areas for further investigation.

## 🐍 Python Data Analysis

The Python workflow includes:

* Generating reproducible synthetic hospital datasets.
* Loading patient, doctor, and encounter data using Pandas.
* Checking missing values and duplicate identifiers.
* Processing dates and numerical columns.
* Creating analytical features and risk-related categories.
* Exploring distributions and relationships between variables.
* Visualizing readmission patterns and healthcare costs.
* Exporting a feature-engineered CSV for Power BI.

## 📈 Power BI Dashboard

The Power BI report uses the feature-engineered encounter dataset to support interactive healthcare analysis.

The prepared data enables reporting on:

* Readmission trends
* Patient demographics
* Diagnosis categories
* Length of stay
* Treatment costs
* Medication and comorbidity patterns
* Previous admissions
* Patient risk segments

The dashboard can help users explore hospital performance from multiple analytical perspectives.

## ⚙️ How to Run the Project

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Replace the placeholder with your actual repository URL.

### 2. Navigate to the Project Folder

```bash
cd Hospital_Readmission_Patient_Flow_Analytics
```

### 3. Install Python Dependencies

```bash
python -m pip install pandas numpy matplotlib seaborn
```

### 4. Generate the Datasets

```bash
python generate_data.py
```

This script generates the synthetic patient, doctor, and encounter datasets.

**Important:** Run the data-generation script before the analysis script if the required CSV files do not already exist. Regenerating the data may replace existing CSV files.

### 5. Run Exploratory Data Analysis

```bash
python eda.py
```

The script performs data quality checks, creates analytical features, generates charts, and exports analysis outputs.

### 6. Set Up the SQL Database

* Open your SQL database client.
* Create or select a database for the project.
* Run `01_create_tables.sql` to create the required tables.
* Import the CSV files into their corresponding tables.
* Preserve identifiers as strings and ensure date and numeric columns use appropriate data types.
* Execute the relevant queries from `02_business_questions.sql`.

### 7. Open the Power BI Report

Open the `.pbix` file in Power BI Desktop.

If prompted, update the data source to use the local project files. Load `encounters_features_powerbi.csv` or configure the model according to the existing report.

Refresh the report after verifying the data source and column mappings.

## 💡 Business Value

This project demonstrates how healthcare data can be organized and analyzed to:

* Monitor readmission patterns.
* Understand patient-flow trends.
* Investigate the relationship between hospital stays and costs.
* Segment patients for further risk analysis.
* Support evidence-based operational planning.
* Present complex data through interactive reporting.

The findings should be interpreted as analytical observations from synthetic data, not as clinical conclusions or recommendations for individual patients.

## 🚀 Future Enhancements

* Add an interactive web application for hospital analytics.
* Develop and validate a machine-learning model for readmission risk prediction.
* Add automated data-quality checks.
* Implement scheduled data refreshes.
* Improve dashboard navigation and drill-through analysis.
* Add a documented set of validated business KPIs.

## 👨‍💻 Author

**Yashraj Rajput**

B.Tech — Data Science

**Areas of Interest:** Data Analytics | Business Intelligence | SQL | Python | Power BI

---

⭐ If you find this project useful, feel free to explore the repository and share feedback.
