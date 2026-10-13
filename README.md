# Banking Customer EDA

Exploratory Data Analysis of 3,000 bank customers using Python, Pandas, Seaborn and Matplotlib. The project looks at income, deposits, loans, savings and loyalty segments, and ends with business recommendations.

## Project Overview

The goal of this project is to understand who the bank's customers are, how their income relates to their balances, and which customer segments deserve attention. The analysis covers data quality checks, univariate and bivariate analysis, outlier detection and correlation analysis.

## Dataset

- **File:** `Banking.csv`
- **Size:** 3,000 rows and 26 columns
- **Data quality:** no missing values and no duplicate rows
- **Numerical columns:** Estimated Income, Superannuation Savings, Credit Card Balance, Bank Loans, Bank Deposits, Checking Accounts, Saving Accounts
- **Categorical columns:** Nationality, Occupation, Fee Structure, Loyalty Classification, Properties Owned, Risk Weighting, Income Band (created during analysis)

## Tools Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Google Colab

## Analysis Steps

1. Loaded the data and checked shape, missing values and duplicates
2. Created an **Income Band** column (Low, Med, High) with `pd.cut`
3. Analyzed the distribution of categorical columns with count plots
4. Analyzed numerical columns with histograms, boxplots and summary statistics
5. Measured skewness and counted outliers using the IQR method
6. Built a correlation heatmap for the numerical columns
7. Compared average balances across Income Bands

## Key Findings

- **Clean data:** 3,000 rows, 26 columns, no missing values, no duplicates.
- **Income is right-skewed:** the mean income (about ₹1.71 lakh) is above the median (about ₹1.42 lakh), with a skewness of 0.88.
- **Most customers are middle income:** 51% are in the Med band, 34% in Low and 15% in High.
- **Outliers are concentrated in balances:** Saving Accounts (5.2%), Bank Deposits (5.0%) and Checking Accounts (4.6%) have the most outliers. They appear to be genuine high-value customers, so they were kept in the data.
- **Strongest relationships:** Bank Deposits is closely related to Checking Accounts (0.84) and Saving Accounts (0.75). Estimated Income and Superannuation Savings are moderately related (0.37).
- **Deposits grow slower than income:** the High band has about 5.8x the income of the Low band but only about 1.9x the deposits.
- **Customer base:** 44% European, 25% Asian and 17% American. 44% of customers are in the Jade loyalty tier, followed by Silver (26%) and Gold (20%).

## Income Band Comparison

| Band | Avg Income | Avg Bank Deposits | Avg Bank Loans | Avg Credit Card Balance |
|------|-----------|-------------------|----------------|--------------------------|
| Low | 64,689 | 4.86 lakh | 4.36 lakh | 2,349 |
| Med | 1,82,132 | 7.19 lakh | 6.21 lakh | 3,345 |
| High | 3,75,405 | 9.30 lakh | 8.41 lakh | 4,478 |

## Business Recommendations

1. **Monitor repayment risk in the Low band**, where average loans are close to average deposits.
2. **Target the Med band** (the largest segment) with savings and investment campaigns.
3. **Offer wealth management products to the High band**, where deposits grow much more slowly than income.
4. **Run upgrade incentives** to move Jade customers into Silver and Gold tiers.

## Next Steps

- Group Occupation into broader categories and analyze it against income and deposits
- Compare Loyalty Classification and Risk Weighting against balances
- Add a saving ratio (deposits divided by income) to compare saving behavior across segments

## How to Run

1. Clone this repository or download the files
2. Open `Banking_EDA.ipynb` in Google Colab or Jupyter Notebook
3. Make sure `Banking.csv` is in the same folder (or upload it in Colab)
4. Run all cells

## Author

**Mohammad Ashfaq**
