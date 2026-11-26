Power BI Financial Dashboard Credit Card
# Credit Card Financial Dashboard

An end-to-end data analytics project using **PostgreSQL, Power BI and
DAX** to explore credit card transactions, financial performance and
customer segments.

## Project objective

Build an interactive dashboard that helps stakeholders monitor credit
card performance, compare customer segments and explore transaction
trends.

## Business questions

-   How much revenue, interest and transaction activity are represented
    in the dataset?
-   Which card categories contribute the most revenue?
-   Which expenditure types generate the most revenue?
-   How does revenue vary by education and customer job?
-   How do swipe, chip and online transactions compare?
-   How does revenue and transaction count vary by quarter?

## Tools

-   **PostgreSQL:** database and CSV import
-   **Power BI Desktop:** data model and dashboard
-   **DAX:** calculated columns and measures

## Data

  -----------------------------------------------------------------------
  Table                               Contents
  ----------------------------------- -----------------------------------
  `cc_detail`                         Card category, annual fees, credit
                                      limit, transaction amount/count,
                                      interest, expenditure type and week
                                      start date

  `cust_detail`                       Customer age, gender, education,
                                      marital status, state, job and
                                      income
  -----------------------------------------------------------------------

The tables are intended to be related through `Client_Num`, with
`cust_detail` on the one side and `cc_detail` on the many side, provided
the customer ID is unique in `cust_detail`.

## Work completed

1.  Created PostgreSQL database tables.
2.  Imported the CSV datasets into PostgreSQL.
3.  Connected Power BI to PostgreSQL.
4.  Modelled customer and credit-card data using `Client_Num`.
5.  Created DAX calculations for age groups, income groups, revenue and
    weekly revenue comparisons.
6.  Built visuals for KPIs, quarterly performance, card category,
    expenditure type, education, customer job and chip usage.

## DAX concepts used

`SWITCH(TRUE())`, `WEEKNUM()`, `CALCULATE()`, `FILTER()`, `ALL()`,
`SUM()` and `DIVIDE()`.

The project's `Revenue` calculation is:

`Annual_Fees + Total_Trans_Amt + Interest_Earned`

This is the metric definition used in this project.

## Dashboard snapshot

  KPI                    Value displayed
  -------------------- -----------------
  Total Revenue                    55.4M
  Total Interest                    7.9M
  Transaction Amount                 45M
  Transaction Count                 657K

## Business Insights

Based on the analysis of credit card transactions and customer demographics, we gained the following insights:

1. **Overall Revenue:** The business generated approximately $55.4M in revenue, with total interest earnings of approximately $7.9M.

2. **Card Category:** Blue credit cards contribute the highest revenue, followed by Silver, Gold and Platinum cards.

3. **Expenditure Patterns:** Bills represent the highest revenue-generating expenditure category, followed by Entertainment, Fuel and Grocery.

4. **Customer Education:** Graduate customers contribute the largest share of revenue among different education groups.

5. **Customer Occupation:** Self-employed customers generate the highest revenue, followed by Businessmen and Blue-collar professionals.

6. **Transaction Methods:** Swipe transactions contribute the highest revenue, followed by Chip and Online transactions.

7. **Quarterly Performance:** Q3 records the highest revenue and transaction count, while Q4 records the lowest revenue.

8. **Gender Analysis:** Male customers contribute approximately $31M in revenue, compared to $26M from female customers.

9. **Geographical Analysis:** Texas, New York and California together contribute approximately 68% of the overall revenue.

10. **Customer Activation:** The overall customer activation rate is approximately 57.5%, while the delinquency rate stands at 6.06%.

### Conclusion

The analysis highlights the major revenue-generating customer segments, popular expenditure categories and transaction patterns. These insights can help the business understand customer behaviour, identify its strongest-performing segments and make more informed decisions regarding customer engagement and credit card services.
