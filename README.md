# E-Commerce Performance Analysis | Power BI

An interactive Power BI analysis of e-commerce orders, sales, reported profit, product categories, geography and payment methods. The project combines order-level information with transaction line items to explore differences in performance across markets and product lines.

## Project at a glance

- **Tools:** Power BI Desktop, Power Query and DAX.
- **Data:** 500 orders and 1,500 line items, dated January–December 2018.
- **Report:** Six pages containing charts, scatter plots, gauges and category comparisons.
- **Analysis:** Regional sales, product profitability, payment modes, monthly performance and customer distribution.

## Data and verified totals

The two included CSV files join on `Order ID`. Independent checks of the files found 500 unique order IDs, no unmatched line items, total `Amount` of 437,771, total reported `Profit` of 36,963 and 5,615 units. The accompanying report describes the monetary values in Indian rupees; the dataset itself does not independently document its currency or provenance.

| File | Grain | Key fields |
| --- | --- | --- |
| `Orders.csv` | One row per order | Order ID, Order Date, CustomerName, State, City |
| `Details.csv` | One row per line item | Order ID, Amount, Profit, Quantity, Category, Sub-Category, PaymentMode |

The CSVs contain 336 distinct customer-name values, 19 distinct state values and 25 distinct city values. Customer names are identifiers in the source data and do not necessarily represent verified unique people.

## Repository structure

```text
ecommerce_performance.pbix   Power BI report and model
Orders.csv                      Order-level source data
Details.csv                     Transaction line items
Empirical Performance Audit.docx  Original analysis report
REQUIREMENTS.md                      Software and data requirements
```

## Open and refresh

1. Install a current version of **Power BI Desktop for Windows**.
2. Download or clone this repository, keeping the files together.
3. Open `ecommerce_performance.pbix` in Power BI Desktop.
4. If prompted about missing source files, select **Transform data** → **Data source settings** and update the paths for `Orders.csv` and `Details.csv` to the local files in the repository folder. Depending on the query, you may instead need to edit the **Source** step in Power Query.
5. Apply changes and refresh. Check the date format and data types if your regional settings interpret dates differently: the supplied order dates use day-month-year.

The PBIX retains its original saved data model and may reference paths from the author's computer. Source-path updates are therefore likely to be required on another machine. The project has not been tested with every Power BI Desktop version or regional configuration.

## Interpretation and limitations

- Profit is the value supplied in the dataset; it should not automatically be treated as independently verified net profit or cash flow.
- The data covers one calendar year, so monthly differences do not establish recurring seasonality.
- Geographic and payment-method comparisons are descriptive. Shipping, returns, discounts and transaction fees are not present in the CSVs, so the causes of differences cannot be established from these files.
- The original document contains hypotheses and recommendations; treat them as proposals for investigation rather than verified causal findings.
- The data source, license and permission for redistribution were not documented in the supplied folder. Verify those rights before distributing the data publicly.

## Author

Shreyas Kamat · [GitHub](https://github.com/TYTKL456) · [LinkedIn](https://www.linkedin.com/in/shreyas-kamat-74a851450/)
