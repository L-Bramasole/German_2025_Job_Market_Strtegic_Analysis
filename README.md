# 🇩🇪 German Job Market 2025: A Strategic Data Analysis
## 🎯 Project Overview
This project provides a comprehensive, data-driven analysis of the German job market, focusing on trends leading up to and during 2025. It integrates job market metrics with historical employment data to deliver actionable insights on demand, salary expectations, and qualification requirements.
The primary goal is to identify strategic career pathways and provide predictive context for stakeholders (job seekers, educators, and hiring managers).
This project is submitted as a student case study, developed as part of a Data Analysis course, with the primary purpose of demonstrating and applying statistical, machine learning, and visualization techniques.
## Key Questions Addressed:
    • Which industries and regions are experiencing the highest demand and growth?
    • What factors (e.g., experience, industry, location) are the strongest predictors of salary?
    • How is the job market segmented in terms of salary vs. volume of opportunities?
    • What is the long-term forecast for German employment trends?
    
## 💾 Data Sources
The analysis is built on two primary datasets:
    1. Job Market 2025 Dataset (Synthetic): A comprehensive set of over 30,000 synthetic job postings data, including job titles, industries, experience levels, salary median, remote availability, and key metrics like a Demand Index and Competitiveness Score.
    2. German Employment Time Series (2010–2025): Real-world historical data on employment numbers from the German Labour Force Survey (Source: Statistisches Bundesamt), used for time series analysis and forecasting.

## 🔬 Methodology and Modeling
The analysis employed a multi-faceted approach to extract meaningful insights:
1. Exploratory Data Analysis (EDA)
Initial analysis focused on descriptive statistics, correlation matrices, and specialized visualizations (e.g., geospatial maps, heatmaps) to profile demand distribution and salary variance across regions, industries, and experience levels.
2. Machine Learning for Prediction and Clustering
    • Linear Regression: Used to quantify the impact of variables (like Experience, Industry, and Remote Availability) on Median Salary.
        ◦ Finding: Experience Level was found to be the single strongest predictor of salary, explaining approximately 57% of the observed variance.
    • K-Means Clustering: Applied to segment the job market based on a combination of features (Salary, Experience, Demand Index, Competitiveness Score).
        ◦ Finding: The market clearly splits into a "Lucrative but Scarce" cluster (High Salary/Experience, Low Volume) and a "Modest but Abundant" cluster (Low Salary/Experience, High Volume).
3. Time Series Forecasting
    • Data Preparation: The historical German employment data was analyzed for stationarity and seasonality. A 12-month lag seasonal differencing was applied to achieve statistical stationarity.

## 💡 Key Findings and Recommendations for Job Applicants
### Strongest Indicators
Metric      	Primary Finding	Strategic                           Implications for Job Applicants
Salary Driver	Experience Level explains ~57% of salary variance.	        Prioritize roles with clear upward mobility.
Top Demand	    IT and Engineering lead in job openings and Demand Index.	Target these sectors for long-term growth and stability.
Salary Hubs	    Berlin and Hessen offer the most competitive median salaries to match the high living expenses.	Location is not a key factor in terms of compensation
Qualifications	Bachelor's and Master's degrees are the standard requirements.	Education is the baseline for entry into most roles.
Remote Work	    Remote availability does not significantly affect the offered median salary.	No penalty for seeking remote work based on pay.
### Market Segmentation (Cluster Analysis)
The market is not homogenous, with distinct segments defining career pathways:
    • Cluster 2 (Lucrative & Scarce): High salaries, high experience, and high competition (e.g., specialized senior IT roles).
    • Cluster 1 (Modest but Abundant): High volume of openings, high demand index, but lower median salaries (e.g., entry-level positions and high-turnover roles).
    
## 🛠️ Repository Structure
.├── README.md                                   // Project overview and documentation.
├── 02 Data/
│   ├── Original/
│   │   ├── german_cities.geojson               // Geospatial data for German cities.
│   │   ├── german_states.geojson               // Geospatial data for German states.
│   │   ├── Job_Market_Germany_dataset.csv      // Primary synthetic job market dataset.
│   │   └── German_employment_2010_2025.xlsx    // Historical employment data (2010–2025).
│   └── Manipulated/
│       ├── Job_Market_Germany_dataset.xlsx     // Cleaned and formatted dataset.
│       ├── Job_Market_Germany_dataset_clustered.xlsx // Clustered dataset (K-Means results).
│       └── Job_Market_Germany_dataset_encoded.xlsx   // Encoded dataset for modeling.
├── 03 Scripts/
│   ├── Set1_01_Cleaning_and_Descriptive.ipynb  // Data profiling, cleaning, and descriptive analysis.
│   ├── Set1_02_Salary_and_Openings_Trends.ipynb // Salary and job openings trend analysis.
│   ├── Set1_03_Geospatial_Analysis.ipynb       // Distribution of jobs across German states and cities.
│   ├── Set1_04_Job_Market_Regressions_Part1.ipynb // Regression modeling (part 1).
│   ├── Set1_04_Job_Market_Regressions_Part2.ipynb // Regression modeling (part 2).
│   ├── Set1_05_Classification_KMeans.ipynb     // K-Means clustering for market segmentation.
│   └── Set2_01_TimeSeries_Analysis_German_Employment.ipynb // Time-series forecasting of employment trends.
├── 04 Analysis/                                // Graphs, tables, and visualization outputs.
├── 05 Results_Summary/                         // Final summarized results of all figures and analyses.
├── src/                                        // Reusable Python modules.
│   ├── data_processor.py                       // Functions for data cleaning and feature engineering.
│   └── visualizer.py                           // Helper functions for generating complex plots.
└── requirements.txt                            // Python dependencies required to run the notebooks.


## ⚙️ Dependencies
To run this project locally, please install the following Python packages:
pip install -r requirements.txt
Required packages include:
    • pandas
    • numpy
    • scikit-learn (for Regression and K-Means Clustering)
    • statsmodels (for Time Series Analysis)
    • matplotlib
    • seaborn
    • geopandas (or similar for geospatial plotting, if used)
