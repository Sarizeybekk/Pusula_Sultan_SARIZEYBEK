Sultan Sarızeybek  
Email: sultansrzybk@gmail.com

## Project : Physical Medicine & Rehabilitation Dataset – EDA & Data Preprocessing  

## Project Overview
This project analyzes a physical medicine & rehabilitation dataset containing **2,235 observations** and **13 features**.  
The primary objective is to make the dataset model-ready with respect to the target variable **`TedaviSuresi` (Treatment Duration)**.  

## Dataset Information
- Number of records: 2,235  
- Number of features: 13  
- Target variable: `TedaviSuresi` (treatment duration in sessions)  

### Column Descriptions
| Column Name        | Description                                  |
|--------------------|----------------------------------------------|
| HastaNo            | Anonymized patient ID                        |
| Yas                | Age                                          |
| Cinsiyet           | Gender                                       |
| KanGrubu           | Blood type                                   |
| Uyruk              | Nationality                                  |
| KronikHastalik     | Chronic conditions (comma-separated)         |
| Bolum              | Department / Clinic                          |
| Alerji             | Allergies (single or comma-separated)        |
| Tanilar            | Diagnoses                                    |
| TedaviAdi          | Treatment name                               |
| TedaviSuresi       | Treatment duration (sessions) – Target       |
| UygulamaYerleri    | Application sites                            |
| UygulamaSuresi     | Application duration                         |

## Tasks

### 1. Exploratory Data Analysis (EDA)
- Inspected data structure and variable types  
- Identified anomalies and missing data  
- Created visualizations (histograms, scatter plots, box plots, heatmaps)  
- Explored relationships between `TedaviSuresi` and other features  

### 2. Data Preprocessing
- Missing values:  
  - Numerical → Iterative Imputer (MICE), Median Imputation  
  - Categorical → Added “Missing” category, category grouping strategies  
- Feature Engineering:  
  - Age groups (0–18, 19–30, 31–45, 46–60, 61–75, 76+)  
  - Blood type split into (A, B, AB, 0) and Rh factor (+/–)  
  - Nationality grouped into “Turkey” vs “Other”  
  - Chronic condition flags (binary) and counts  
  - Allergy presence as binary feature  
- Categorical Encoding:  
  - Low cardinality → OrdinalEncoder  
  - High cardinality → Frequency Encoding  
- Numerical Processing:  
  - Missing value handling with Iterative Imputer  
  - Scaling with RobustScaler (robust against outliers)  

###  Pipeline Code
- Implemented with Pipeline & ColumnTransformer  
- Ensures modularity, reusability, and reproducibility
## Documentation

<embed src="case_study_report.pdf" width="100%" height="600px" type="application/pdf">


