# Retail Sales & UK Employment Analysis Dashboard

This repository contains the source data and analytical outputs for two distinct projects: **Retail Sales Performance Analysis** (Excel-based tasks) and **UK Job Change Analysis** (Data and associated Tableau/Power BI dashboard).

The primary goal is to provide a complete record of the source data structure and the purpose of the key visualizations across all sheets and the final dashboard.

---

## 💾 Data Sources

The analysis draws upon two main Excel files and one dashboard file:

1.  **`retail_sales_dataset_Master.xlsx`**: Contains raw transaction data and smaller datasets used for hands-on Excel exercises (Pivot Tables, Functions, etc.).
2.  **`EMSI_JobChange_UK.xlsx`**: Contains detailed employment figures for various UK cities and industries, segmented by broad and detailed industry codes.
3.  **`Employment Dataset.twbx`**: The final interactive Tableau/Power BI dashboard visualizing the UK Job Change data.

---

## 📋 Data Dictionary: Excel Sheet Details

The following table provides an overview of the purpose and key fields within each extracted sheet/CSV file:

| File Name | Data Type | Key Columns | Purpose / Focus |
| :--- | :--- | :--- | :--- |
| `retail_sales_dataset.csv` | **Raw Transactional Data** | `Date`, `Product Category`, `Gender`, `Generation`, `Total Sales` | The core dataset for trend analysis and detailed customer/product segmentation. |
| `retail_sales_dataset_Master.xlsx - Sheet1.csv` | **Pivot Table (Proportional)** | `Product Category`, `Gender`, `Generation` (Values are **percentages** of total sales) | Shows the distribution of market share across gender and generation segments for each product. |
| `retail_sales_dataset_Master.xlsx - Sheet2.csv` | **Pivot Table (Absolute)** | `Product Category`, `Gender`, `Adult` (Values are **absolute sales** figures) | Summarizes absolute sales figures, typically filtered or focused on a specific segment (e.g., the 'Adult' generation). |
| `retail_sales_dataset_Master.xlsx - Day 2 Task 2.csv` | **Student Scores** | `Student name`, `English`, `Mathematics`, `Science`, `Average` | Data used for Excel functional tasks like calculating `AVERAGE` and `MAX` values, and practice with sorting and filtering. |
| `retail_sales_dataset_Master.xlsx - Transactions.csv` | **Utility/Demo** | `Total Sales`, `Product category`, `Concatenate` | A small dataset demonstrating text manipulation and concatenation functions. |
| `EMSI_JobChange_UK.xlsx - 1 digit.csv` | **Employment Data (Broad)** | `City`, `SIC Code`, `Industry`, `Jobs 2011`, `Jobs 2014`, `% Change` | Job change data aggregated by **1-digit** Standard Industrial Classification (SIC) codes for a high-level industry overview. |
| `EMSI_JobChange_UK.xlsx - 2 digit.csv` | **Employment Data (Detailed)** | `City`, `SIC-2`, `Industry`, `Jobs 2011`, `Jobs 2014`, `% Change` | Job change data aggregated by the granular **2-digit** SIC code for deeper sector-specific insight. |

---

## 📊 Visualization Overview

### Retail Sales Data Visualizations (Charts from Sheets)

The following chart types were either present in the original Excel file or are the most appropriate representations of the data within those sheets:

| Sheet/Analysis | Recommended Chart Type | Analytical Purpose |
| :--- | :--- | :--- |
| **`retail_sales_dataset.csv`** (Raw Data) | **Line Chart (Time Series)** | Illustrates the **Sales Trend Over Time** (Daily Sum) to identify seasonal patterns and performance volatility. |
| **`Sheet1.csv`** (Proportional) | **100% Stacked Column Chart** | Used to compare the **Proportional Market Share** of different `Gender`/`Generation` segments within each `Product Category`. |
| **`Sheet2.csv`** (Absolute) | **Clustered Bar Chart** | Compares **Absolute Sales** by `Product Category` across different dimensions (e.g., `Gender` or `Generation`) to identify key revenue drivers. |
| **`Day 2 Task 2.csv`** (Student Scores) | **Ranked Bar Chart** | Provides a clear visual ranking of **Student Performance** based on the calculated `Average Score`. |

### UK Job Change Dashboard (`Employment Dataset.twbx`)

The core of the UK Job Change project is the interactive dashboard, which is built on the `EMSI_JobChange_UK.xlsx` data.

1.  **Geographic Map of Job Change**:
    * **Description**: A Choropleth Map of the UK where cities are colored based on the overall **% Change** in jobs between 2011 and 2014. 
    * **Purpose**: Allows for quick identification of regional economic hotspots and areas of job market decline.

<img width="1528" height="640" alt="image" src="https://github.com/user-attachments/assets/ba955628-2fd9-473c-82ce-c52ac9910059" />


2.  **Industry Ranking Chart**:
    * **Description**: A **Ranked Bar Chart** displaying the **Change** or **% Change** in jobs for the top and bottom performing **1-digit Industries**.
    * **Purpose**: Highlights the most impactful broad sectors contributing to the national job market shift.

<img width="1448" height="653" alt="image" src="https://github.com/user-attachments/assets/dacc5fa3-8a6d-463a-a888-28debaf7a91b" />

3.  **Detailed Industry Comparison**:
    * **Description**: Charts that allow filtering and drill-down into the highly specific **2-digit Industries** (e.g., comparing specific manufacturing sub-sectors or professional services).
    * **Purpose**: Provides granularity for deep-dive analysis into specific economic sectors' performance.
<img width="1614" height="643" alt="image" src="https://github.com/user-attachments/assets/455804af-bea9-4436-bdf1-936e0cf139da" />

4.  **Key Performance Indicators (KPIs)**:
    * **Description**: Large summary boxes displaying the overall **Total Jobs 2014**, **Total Change**, and **Total % Change** across the entire dataset.
    * **Purpose**: Offers an immediate, high-level summary of the entire job market's health.

<img width="1421" height="653" alt="image" src="https://github.com/user-attachments/assets/c5055b03-7356-419a-811c-a5bd0657b764" />
