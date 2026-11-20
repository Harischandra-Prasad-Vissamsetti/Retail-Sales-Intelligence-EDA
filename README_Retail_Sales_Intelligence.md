# Retail Sales Intelligence: Exploratory Data Analysis & Data Visualization

An end-to-end Python data analytics project focused on exploring retail sales data, evaluating business performance, identifying trends, and uncovering patterns in sales, profitability, regional performance, product categories, and discount activity.

This project was developed as part of the **CodeAlpha Data Analytics Internship – Task 2 and Task 3**. It uses the Kaggle Superstore dataset and demonstrates a structured Exploratory Data Analysis (EDA) workflow, from data inspection and cleaning to KPI calculation and visualization.

<p align="center">
  <a href="https://github.com/Harischandra-Prasad-Vissamsetti/Retail-Sales-Intelligence-EDA">
    <strong>GitHub Repository</strong>
  </a>
  &nbsp;|&nbsp;
  <a href="https://www.kaggle.com/datasets/vivek468/superstore-dataset-final">
    <strong>Dataset</strong>
  </a>
</p>

---

## Table of Contents

- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [Dataset Information](#dataset-information)
- [Repository Structure](#repository-structure)
- [How to Access the Project](#how-to-access-the-project)
- [How to Run the Project in Google Colab](#how-to-run-the-project-in-google-colab)
- [Analysis Workflow](#analysis-workflow)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Business KPIs](#business-kpis)
- [Analysis and Visualizations](#analysis-and-visualizations)
- [Business Questions Explored](#business-questions-explored)
- [Results and Interpretation](#results-and-interpretation)
- [Limitations](#limitations)
- [Future Enhancements](#future-enhancements)
- [Author](#author)
- [Acknowledgements](#acknowledgements)

## Project Overview

Retail businesses generate transaction data that can provide valuable insights into sales performance, profitability, customer segments, product categories, and regional trends.

The purpose of this project is to analyze a Superstore retail dataset using Python. The notebook performs data quality checks, prepares the data for analysis, calculates key business performance indicators, and creates visualizations to make patterns easier to understand.

The analysis is exploratory. It helps identify trends and relationships in the available data; it does not claim that observed associations prove cause and effect.

**Project details**

| Item | Description |
|---|---|
| Project name | Retail Sales Intelligence: EDA & Data Visualization |
| Internship | CodeAlpha – Data Analytics |
| Tasks | Task 2 and Task 3 |
| Project type | Exploratory Data Analysis and Data Visualization |
| Programming language | Python |
| Development environment | Google Colab / Jupyter Notebook |
| Dataset | Superstore Dataset Final – Kaggle |

## Objectives

- Understand the structure and quality of the retail dataset.
- Identify missing values, duplicate records, and data type issues.
- Clean and prepare data for reliable analysis.
- Calculate important sales and profitability KPIs.
- Compare performance across categories, sub-categories, regions, and customer segments.
- Explore monthly sales, profit, and order trends.
- Investigate discount patterns and their relationship with profit.
- Communicate findings through clear tables and visualizations.

## Key Features

- Dataset inspection and descriptive statistical analysis.
- Missing-value and duplicate-record assessment.
- Standardization of column names and conversion of date and numeric fields.
- Removal of exact duplicate rows and records missing essential analysis fields.
- Calculation of sales, profit, profit margin, unique orders, customer count, average discount, and average quantity where the source columns are available.
- Category, sub-category, regional, and customer-segment performance summaries.
- Monthly sales and profit trend analysis.
- Discount-band comparisons and discount-versus-profit visualization.
- Final data-quality report for the cleaned dataset.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Pandas | Data manipulation, cleaning, and analysis |
| NumPy | Numerical calculations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Google Colab | Cloud-based notebook execution |
| Jupyter Notebook | Interactive development environment |

## Dataset Information

**Dataset:** [Superstore Dataset Final – Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

The project uses a publicly available Kaggle Superstore dataset. Download the CSV from the dataset page before running the notebook.

The notebook checks for these essential columns after standardizing column names:

| Original column | Standardized column | Purpose |
|---|---|---|
| Order ID | `order_id` | Identify orders |
| Order Date | `order_date` | Analyze order dates and monthly trends |
| Sales | `sales` | Calculate sales performance |
| Profit | `profit` | Evaluate profitability |
| Category | `category` | Compare product categories |
| Region | `region` | Compare regional performance |

Additional columns such as `customer_id`, `segment`, `sub_category`, `quantity`, `discount`, and `ship_date` are used when available.

**Dataset attribution:** Vivek Chowdhury, *Superstore Dataset Final*, Kaggle. Please review the dataset page's license and terms before redistributing the dataset or using it commercially. The dataset is not included in this repository by default.

## Repository Structure

```text
Retail-Sales-Intelligence-EDA/
│
├── README.md
│
├── Retail_Sales_Intelligence_Colab_File.ipynb
│
└── (Dataset downloaded separately from Kaggle)
    └── Sample - Superstore.csv
```

The CSV is kept separate because it is sourced from Kaggle. The notebook is the main project file.

## How to Access the Project

### Option 1: Access through GitHub

1. Open the project repository:

   [Retail Sales Intelligence – GitHub Repository](https://github.com/Harischandra-Prasad-Vissamsetti/Retail-Sales-Intelligence-EDA)

2. Open `Retail_Sales_Intelligence_Colab_File.ipynb`.
3. Download the notebook using GitHub's download option, or clone the repository using Git.
4. Download the dataset from the Kaggle link in the [Dataset Information](#dataset-information) section.
5. Follow the Google Colab instructions below to execute the notebook.

### Option 2: Clone the repository

Make sure Git is installed, then run:

```bash
git clone https://github.com/Harischandra-Prasad-Vissamsetti/Retail-Sales-Intelligence-EDA.git
```

Move into the project directory:

```bash
cd Retail-Sales-Intelligence-EDA
```

Download the Kaggle CSV separately and follow the dataset setup instructions below.

## How to Run the Project in Google Colab

Google Colab is the recommended way to run this notebook because it is designed around the Colab environment.

### Step 1: Download the dataset

1. Visit the [Superstore Dataset Final on Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final).
2. Sign in to Kaggle if required.
3. Download the dataset.
4. Extract the downloaded archive if it is compressed.
5. Locate the CSV file.

### Step 2: Open the notebook in Google Colab

1. Visit [Google Colab](https://colab.research.google.com/).
2. Sign in with your Google account.
3. Select **File → Upload notebook**.
4. Upload `Retail_Sales_Intelligence_Colab_File.ipynb` from the downloaded repository.

### Step 3: Upload the dataset to the Colab runtime

The notebook's active data-loading statement expects this exact path and filename:

```python
raw_df = pd.read_csv("/content/Sample - Superstore.csv", encoding="latin-1")
```

To satisfy it:

1. In Colab, open the **Files** panel on the left.
2. Click **Upload to session storage**.
3. Select the downloaded CSV.
4. Ensure the uploaded file is named exactly `Sample - Superstore.csv`.
5. Confirm that it appears in the `/content/` directory.

If your downloaded CSV has a different name, either rename it to `Sample - Superstore.csv` before uploading or update the path in the notebook's data-loading cell.

### Step 4: Install and import libraries

Run the notebook's first setup cells. The notebook installs the required packages:

```python
!pip -q install pandas numpy matplotlib seaborn
```

The remaining setup cell imports the libraries used for the analysis.

### Step 5: Execute the notebook

1. Select **Runtime → Run all** in Google Colab, or execute cells one at a time.
2. Run the cells from top to bottom.
3. Review the displayed data-quality summaries, KPI tables, grouped analysis, and charts.
4. Read the final sections and write conclusions based on the actual output generated by your run.

**Important:** The notebook includes an example interactive `files.upload()` workflow in comments, but the active data-loading code uses the `/content/Sample - Superstore.csv` path. Upload the file to that path or change the active code before running.

## Analysis Workflow

The project follows these stages:

1. **Environment setup:** Install and import Python libraries.
2. **Dataset loading:** Read the Kaggle CSV file into a Pandas DataFrame.
3. **Business questions:** Define questions about sales, profit, orders, categories, regions, discounts, and data quality.
4. **Data inspection:** Review dataset dimensions, data types, descriptive statistics, missing values, and unique values.
5. **Data cleaning:** Standardize column names, parse dates, convert numeric fields, remove exact duplicates, and exclude records missing essential fields.
6. **KPI calculation:** Calculate key business performance indicators.
7. **Performance analysis:** Compare categories, regions, segments, and sub-categories.
8. **Time-series analysis:** Aggregate sales, profit, and unique orders by month.
9. **Visualization:** Create category, regional, and sub-category performance charts.
10. **Discount analysis:** Compare discount bands and explore discount-versus-profit patterns.
11. **Validation:** Review numeric correlations and the final data-quality report.
12. **Conclusion:** Interpret the actual results and identify opportunities for further analysis.

## Data Cleaning and Preparation

The notebook applies the following preparation steps:

- Standardizes column names into lowercase, underscore-separated names.
- Checks for required columns: `order_id`, `order_date`, `sales`, `profit`, `category`, and `region`.
- Converts `order_date` and `ship_date` to datetime values when those columns are available.
- Converts `sales`, `profit`, `quantity`, and `discount` to numeric values when available.
- Removes exact duplicate rows.
- Removes records missing essential analysis fields: order ID, order date, sales, profit, category, and region.
- Retains repeated order IDs because one order can contain multiple product-line records.
- Derives order year, order month, and profit margin percentage.
- Calculates shipping days when a ship-date column is available; negative shipping durations are treated as invalid.
- Creates discount bands when a discount column is available.

The notebook displays data-quality summaries before and after cleaning so the effect of these steps can be reviewed.

## Business KPIs

The project calculates the following KPIs when the required source columns are available:

| KPI | Description |
|---|---|
| Transaction line items | Number of records in the cleaned dataset |
| Unique orders | Number of distinct order IDs |
| Unique customers | Number of distinct customer IDs |
| Total sales | Sum of sales values |
| Total profit | Sum of profit values |
| Overall profit margin | Total profit divided by total sales, multiplied by 100 |
| Average discount | Mean discount value |
| Average quantity | Mean quantity per record |

**Profit margin formula:**

```text
Profit Margin (%) = (Total Profit / Total Sales) × 100
```

Transaction line items and unique orders are not the same measure. A single order can contain multiple product-line records.

## Analysis and Visualizations

The notebook produces tables and visualizations to explore the following areas:

### 1. Monthly Sales and Profit Trend

A line chart comparing monthly sales and profit totals. It also calculates the number of unique orders per month.

### 2. Sales vs Profit by Category

A bar chart comparing total sales and total profit across product categories.

### 3. Regional Sales and Profitability

A horizontal bar chart comparing sales and profit across the available regions.

### 4. Profit by Sub-Category

A chart showing total profit for each sub-category, making positive and negative profit contributions easier to identify.

### 5. Discount vs Profit

A scatter plot exploring the relationship between discount and profit. The notebook uses a sample of up to 4,000 records with `random_state=42` for reproducibility.

### 6. Discount-Band Analysis

A grouped summary comparing transaction-line counts, average sales, average profit, and total profit across discount bands.

### 7. Data Quality and Correlation

The notebook displays data-quality summaries and a numeric correlation matrix to help inspect the cleaned dataset and explore associations between numeric variables.

## Business Questions Explored

The analysis is designed to investigate questions such as:

- What are the total sales, total profit, order count, and overall profit margin?
- Which product categories and sub-categories have the highest sales?
- Which categories or sub-categories contribute the most profit or loss?
- Which regions perform best in terms of sales and profitability?
- How do sales and profit change over time?
- What differences appear across customer segments?
- How do discount levels relate to average and total profit?
- Are there missing values, duplicate records, or invalid records that require attention?

## Results and Interpretation

Run the notebook to generate the actual KPI values, summary tables, and visualizations for the dataset version you use.

When interpreting the results, consider the following:

- High sales do not necessarily mean high profitability.
- Negative aggregated profit indicates a loss in the corresponding group and may warrant further investigation.
- A relationship between discount and profit is an association; it does not establish that discounts caused a profit change.
- Compare group averages with transaction counts and business context.
- Base final project conclusions on the generated outputs rather than assumptions.

This README intentionally does not claim fixed sales totals, profit values, or business findings. Those values should be taken from the results produced by executing the notebook.

## Limitations

- The analysis depends on the quality, coverage, and definitions in the supplied Kaggle dataset.
- Missing or unavailable optional columns limit the analyses that can be performed.
- The notebook performs exploratory analysis; it does not establish causal relationships.
- The discount-versus-profit scatter plot uses a sample of up to 4,000 records rather than necessarily plotting every row.
- The notebook's output-export statements are currently commented out, so CSV reports and chart image files are not automatically saved by default.

## Future Enhancements

- Develop an interactive dashboard using Power BI or Tableau.
- Add SQL queries for more advanced business analysis.
- Perform customer RFM segmentation.
- Conduct customer cohort and retention analysis.
- Explore sales forecasting using chronological train/test validation.
- Add automated data-quality checks and reusable reporting functions.
- Enable export of cleaned datasets, KPI summaries, and chart images.

## Author

**Harischandra Prasad Vissamsetti**

- GitHub: [Harischandra-Prasad-Vissamsetti](https://github.com/Harischandra-Prasad-Vissamsetti)
- Project Repository: [Retail-Sales-Intelligence-EDA](https://github.com/Harischandra-Prasad-Vissamsetti/Retail-Sales-Intelligence-EDA)

## Acknowledgements

- **CodeAlpha** – Data Analytics Internship project tasks.
- **Kaggle** – For hosting the Superstore dataset.
- **Python open-source community** – For the libraries used in this project.

---

If you find this project useful, consider giving the repository a star. Suggestions and constructive feedback are welcome.
