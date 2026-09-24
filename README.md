# Supermarket Sales Analysis — Data Analytics Project

**AICTE | IBM SkillsBuild Data Analytics with AI Academic Internship 2026 — BharatCares**
**Author:** Mansi

## Project Description

The aim of this project is to analyze supermarket sales data and find useful information
about **products, branches, categories, customers, payments, and ratings**. The analysis
covers category- and product-level revenue, branch/city performance, customer segmentation
(membership and gender), payment-method usage, and rating patterns, along with a small
predictive-analytics (AI) extension that models transaction sales value.

## Dataset

- **File:** `supermarket_sales_500.csv`
- **Size:** 500 sales transactions
- **Source:** Provided "SUPER MARKET DATA" database for this internship's Master Class
  practice material (Google Sheet, "supermarket_sales_500_rows"). The notebook loads this
  CSV directly — no external download or API key needed.
- **Columns:** Invoice ID, Date, Branch, City, Customer Type, Gender, Product, Category,
  Quantity, Unit Price, Payment, Rating, Sales.
- **Coverage:** 4 branches/cities (Jaipur, Delhi, Mumbai, Bengaluru), 8 product categories
  (Dairy, Grocery, Personal Care, Fruits, Vegetables, Snacks, Beverages, Bakery), 4 payment
  methods (UPI, Net Banking, Card, Cash), transactions dated Jan–Jul 2026.

## Technologies Used

- Python 3
- pandas, numpy — data handling
- matplotlib, seaborn — visualization / EDA
- scikit-learn — Linear Regression & Random Forest (predictive-analytics extension), metrics
- Jupyter Notebook

## Project Structure

```
├── Mansi_SupermarketSalesAnalysis.ipynb   # Main notebook: cleaning, EDA, modeling, insights
├── requirements.txt                        # Python dependencies
├── Mansi_ProjectReport.docx                # Full project report
├── README.md                               # This file
└── supermarket_sales_500.csv               # Dataset used by the notebook
```

## Setup & Run Instructions

1. Download/clone this project folder, keeping `supermarket_sales_500.csv` alongside the
   notebook.
2. (Recommended) Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Launch Jupyter and run the notebook top to bottom:
   ```bash
   jupyter notebook Mansi_SupermarketSalesAnalysis.ipynb
   ```

## Key Results

- **Category performance:** Beverages, Personal Care, and Grocery are the top
  revenue-generating categories; Bakery contributes the least.
- **Branch performance:** Total sales and average transaction value vary across the four
  branches, with the Mumbai branch handling the highest number of transactions.
- **Customers:** Member customers make up 57% of transactions, but average transaction
  value is similar between Member and Normal customers — membership is associated with
  visit frequency more than basket size in this dataset.
- **Payments:** UPI and Net Banking are the most-used payment methods, reflecting a shift
  toward digital payments.
- **Ratings:** Average ratings are consistently around 4 out of 5 across branches and
  payment methods, indicating steady service quality.
- **Predictive component:** A Random Forest regression model predicts transaction Sales
  value from branch, category, customer type, gender, payment, quantity, and unit price
  with very high accuracy (Sales is largely determined by Quantity × Unit Price).

## Future Scope

- Predict customer **Rating** (a genuinely non-deterministic target) from transaction and
  customer attributes to identify drivers of satisfaction.
- Add time-series forecasting of monthly/weekly sales per branch or category.
- Build a customer segmentation model (e.g. RFM analysis) to identify high-value customers.
- Deploy the analysis as an interactive dashboard (e.g. Streamlit or Power BI).

## License

This project was created for academic/internship submission purposes.
