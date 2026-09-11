 # 🍃 Renewable Energy Consumption & Generation Analytics for College Campuses

> **A data analytics project focused on understanding energy consumption, renewable generation, battery performance, weather impact, grid dependency, and maintenance across college campuses in India.**

---

## 📊 Dashboard Preview

<p align="center"> <img src="https://github.com/Hanne-Jenifer/EcoPulse_Renewable_Energy_Analysis/blob/5d74bda97a12a8ca4a36ed1fdfd2906793d655a0/Renewable%20Energy%20Dashboard%20Overview.png" alt="Renewable Energy Dashboard Overview" width="100%"> </p>

<p align="center"> <img src="https://github.com/Hanne-Jenifer/EcoPulse_Renewable_Energy_Analysis/blob/5d74bda97a12a8ca4a36ed1fdfd2906793d655a0/Energy%20Consumption%20Analysis.png" alt="Energy Consumption Analysis" width="100%"> </p>

<p align="center"> <img src="https://github.com/Hanne-Jenifer/EcoPulse_Renewable_Energy_Analysis/blob/5d74bda97a12a8ca4a36ed1fdfd2906793d655a0/Energy%20Performance%20Analytics.png" alt="Energy Performance Analytics" width="100%"> </p>

<p align="center"> <img src="https://github.com/Hanne-Jenifer/EcoPulse_Renewable_Energy_Analysis/blob/0e0fd3843c4563d352ec4fb927349d2329eba668/Operational%20Performance%20Analysis.png" alt="Operational Performance Analysis" width="100%"> </p>

The Power BI dashboard provides an interactive overview of energy consumption, renewable energy performance, and operational performance. The dashboard includes dedicated analytical views for **Energy Consumption Behavior**, **Renewable Energy Performance**, and **Operational Performance**.  


---

## 📌 Project Overview

Government campuses across India consume significant amounts of electricity across classrooms, laboratories, hostels, libraries, and other facilities. With the adoption of solar, wind, and battery storage systems, understanding how energy is consumed and generated becomes increasingly important.

This project analyzes data from **150 campuses across India** to understand:

- Energy consumption patterns
- Renewable energy contribution
- Battery storage performance
- Weather impact on renewable generation
- Grid dependency and import costs
- Maintenance activity and operational performance

The objective is to transform raw energy-related data into meaningful analytical insights that can support more effective energy management.  

---

## 🎯 Business Objectives

The analysis focuses on five major business objectives:

1. **Improve Renewable Energy Generation**
2. **Optimize Energy Consumption**
3. **Improve Battery Performance**
4. **Understand Weather Impact**
5. **Improve Maintenance**

---

## 🗂️ Data Architecture

The project follows a dimensional data structure containing **dimension tables** and **fact tables** covering campus information, energy activity, renewable generation, weather, battery operations, grid transactions, and maintenance.

### Dimension Tables

| Dimension | Purpose |
|---|---|
| `Dim_Campus_150.xlsx` | Campus information, location, population, region and campus type |
| `Dim_Campus_Buildings.xlsx` | Campus building information |
| `Dim_Asset_Master.xlsx` | Renewable and operational asset information |
| `Dim_Load_Category_Master.xlsx` | Energy load category information |
| `Dim_Date_2021_2025.xlsx` | Date dimension |
| `Dim_Time_Hourly.xlsx` | Hourly time dimension |
| `Dim_Emission_Factor_2021_2025.xlsx` | Emission factor information |
| `Dim_State_Renewable_Benchmark.xlsx` | State-level renewable benchmarks |
| `Fact_Campus_Capacity_Master.xlsx` | Campus capacity information |

### Fact Tables

| Fact Table | Coverage |
|---|---|
| Energy Consumption | 2021–2025 |
| Renewable Generation | 2021–2025 |
| Battery Operations | 2021–2025 |
| Grid Transactions | 2021–2025 |
| Weather | 2021–2025 |
| Maintenance | 2021–2025 |

The campus dimension contains **150 records**, **10 columns**, **150 unique campus IDs**, **18 states**, and **5 regions**.  

---

## 🧹 Data Cleaning & EDA

The data preparation workflow included:

### Data Profiling
- Dataset shape and structure analysis
- Data type inspection
- Descriptive statistics
- Missing-value analysis
- Duplicate-record detection
- Category distribution analysis

### Business Rule Validation
The datasets were checked for logical constraints such as:

- Negative energy consumption
- Negative population values
- Invalid occupancy percentages
- Invalid geographic coordinates
- Negative renewable generation
- Invalid capacity utilization values
- Invalid weather dependency scores

### Referential Integrity
Relationships between fact and dimension tables were validated using key-level checks such as:

- `campus_id`
- `load_category_id`

### Missing Value Treatment
Where appropriate, missing numerical values were handled using **median imputation**, while dates and categorical fields were processed according to their data characteristics.

The cleaning workflow also included datatype conversion, duplicate checks, business-rule validation, outlier assessment, and retention of data-quality flags.  

### EDA Techniques

- Distribution analysis
- Box plots
- Histograms
- Category comparisons
- Correlation analysis
- Time-series analysis
- Regional analysis
- Load-category analysis
- Renewable source contribution analysis

---

## 📐 Statistical Analysis

The statistical analysis was designed around business questions rather than only descriptive exploration.

### Methods Used

| Technique | Purpose |
|---|---|
| Descriptive Statistics | Understand typical values and distributions |
| Measures of Dispersion | Evaluate variability |
| Distribution Analysis | Examine skewness and kurtosis |
| Correlation Analysis | Identify relationships between variables |
| Independent t-test | Compare two groups |
| ANOVA | Compare multiple groups |
| OLS Regression | Evaluate predictive relationships |
| Time-Series Analysis | Study changes over time |
| Comparative Analysis | Compare renewable energy sources |

---

## ⚡ Energy Consumption Analysis

The energy consumption analysis examined:

- Energy consumed
- Peak demand
- Occupancy
- Energy cost
- Weekday vs weekend consumption
- Load-category consumption
- Monthly consumption trends

### Key Findings

- Average energy consumption was **697.11 kWh**, while the median was **428.21 kWh**.
- Energy consumption was **right-skewed**, with skewness of **2.38**.
- Energy consumption showed a very strong relationship with **peak demand** and **energy cost**.
- Weekday consumption was higher than weekend consumption:
  - **Weekday:** 783.75 kWh
  - **Weekend:** 479.71 kWh
- The time-series analysis showed variation throughout the year rather than a consistent increasing or decreasing trend.

---

## 🌦️ Weather Analysis

The weather analysis evaluated:

- Temperature
- Humidity
- Solar irradiance
- Wind speed
- Rainfall
- Weather conditions

### Key Findings

- Solar irradiance and rainfall showed a **very strong negative correlation (r = -0.97)**.
- Humidity and solar irradiance showed a **strong negative correlation (r = -0.84)**.
- Humidity and rainfall showed a **strong positive correlation (r = 0.77)**.
- Sunny conditions produced the highest average solar irradiance.
- Rainy conditions produced the lowest average solar irradiance.

The regression model for solar irradiance achieved an **R² of 0.962**, with humidity and rainfall showing statistically significant relationships with solar irradiance in the fitted model.

---

## ☀️ Renewable Energy Analysis

The renewable generation analysis focused on:

- Solar generation
- Wind generation
- Total renewable generation
- Renewable capacity
- Capacity utilization
- Weather dependency
- Maintenance impact
- Monthly generation
- Renewable source contribution

### Key Findings

- Average renewable generation was **2,857.94 kWh**.
- Renewable generation had a correlation of **0.805** with renewable capacity.
- Solar energy contributed approximately **88.07%** of total renewable generation.
- Wind energy contributed approximately **11.93%**.
- **Solar energy was the dominant renewable energy source.**

Weather conditions also had a significant effect on renewable generation, with **Sunny** conditions producing the highest average generation and **Rainy** conditions producing the lowest.

Renewable generation remained relatively high from **January to May**, declined during **June to September**, and increased again from **October to December**.

---

## 🔋 Battery Storage Analysis

The battery analysis examined:

- Charge energy
- Discharge energy
- State of charge
- Battery efficiency
- Battery cycles
- Battery health

### Key Findings

- Average battery efficiency was **95.91%**.
- Battery efficiency remained highly stable throughout the dataset.
- Charge and discharge levels showed a negative relationship (**r = -0.56**).
- Battery efficiency had only weak relationships with charge and discharge levels.
- Battery health categories showed statistically significant differences in mean battery efficiency.
- Monthly analysis indicated a **slight decline in battery efficiency during 2021**, while overall performance remained high.

---

## 🔌 Grid Transaction Analysis

The grid analysis examined:

- Grid imports
- Grid exports
- Import costs
- Export revenue
- Net grid energy
- Grid dependency

### Key Findings

- Average grid import was **2,204.66 kWh**.
- Average grid import cost was **₹15,854.23**.
- Average grid dependency was **39.30%**.
- Grid import and import cost showed a very strong positive correlation (**r = 0.975**).
- Weekday and weekend grid import costs did **not** show a statistically significant difference in the performed t-test.
- Monthly grid import costs fluctuated throughout 2021.

---

## 🛠️ Maintenance Analysis

The maintenance analysis examined:

- Maintenance cost
- Downtime
- Efficiency before maintenance
- Efficiency after maintenance
- Technician hours
- Maintenance type
- Failure severity
- Maintenance status

### Maintenance Types

| Maintenance Type | Activities |
|---|---:|
| Preventive | 4,648 |
| Corrective | 1,988 |
| Emergency | 560 |

### Key Findings

- Average maintenance cost was **₹39,524.05**.
- Average downtime was **11.29 hours**.
- Average efficiency before maintenance was **84.60%**.
- Average efficiency after maintenance was **90.63%**.
- Maintenance cost had strong positive relationships with:
  - Downtime: **r = 0.847**
  - Technician hours: **r = 0.816**
- Maintenance cost showed strong negative relationships with efficiency:
  - Efficiency before maintenance: **r = -0.822**
  - Efficiency after maintenance: **r = -0.704**
- Emergency maintenance had the highest average cost, followed by corrective and preventive maintenance.

---

## 📊 Power BI Dashboard

The final Power BI dashboard converts the analysis into an interactive business intelligence interface.

### Dashboard Structure

#### 1. Dashboard Overview

The landing page presents high-level KPIs including:

- **Total Energy Consumed:** 2,179.28M
- **Renewable Energy Generation:** 287.99M
- **Total Grid Energy Import:** 584.80M
- **Renewable Energy Utilization:** 13.2%

#### 2. Energy Consumption Behavior

Includes:

- Average daily energy consumed
- Average peak demand
- Monthly consumption trend
- Regional consumption
- Load-category consumption
- Campus-type consumption
- Year and weekday/weekend filters

#### 3. Renewable Energy Performance

Includes:

- Total renewable generation
- Renewable energy utilization
- Solar vs wind generation
- Regional generation
- State-level renewable generation
- Monthly renewable generation trend
- Year and region filters

#### 4. Operational Performance

Includes:

- Total grid energy import
- Grid dependency
- Grid import cost
- Grid emission factor
- State-level operational analysis
- Application and installation counts
- Year and region filters

---

## 🧰 Tools & Technologies

### Programming & Analysis
- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **SciPy**
- **Statsmodels**

### Business Intelligence
- **Microsoft Power BI**

### Data & File Formats
- Excel
- Jupyter Notebook
- PDF

---

## 💡 Key Takeaways

The analysis demonstrates that:

- Energy demand varies significantly across time and operating conditions.
- Peak demand and energy consumption are strongly connected.
- Weather conditions have a major influence on solar availability and renewable generation.
- **Solar is the primary contributor to renewable generation.**
- Battery efficiency remains high but shows a slight decline over time.
- Grid dependency remains an important component of overall energy management.
- Maintenance cost, downtime, technician effort, and operational efficiency are strongly interconnected.

---

## 🏁 Conclusion

This project brings together **data cleaning, exploratory data analysis, statistical analysis, and Power BI visualization** to create a comprehensive view of renewable energy and energy consumption across college campuses.

Rather than analyzing energy consumption in isolation, the project connects **demand, renewable generation, weather, battery storage, grid activity, and maintenance** to provide a broader understanding of campus energy performance.

The resulting Power BI dashboard transforms these analytical findings into an interactive decision-support interface for exploring energy behavior and operational performance.

---

## 👤 Author

**Hanne Jenifer**
