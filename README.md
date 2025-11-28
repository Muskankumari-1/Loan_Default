## Loan Default Analysis & Financial Risk Dashboard – Power BI Project

## Problem Statement

Financial institutions need to understand borrower behavior, credit score patterns, income distribution, and default trends to make better lending decisions.
However, raw loan data is complex and spread across multiple categories such as:

Borrower demographics

Employment type

Credit scores

Loan purpose

Income brackets

Yearly default rates

This dashboard provides a complete analytical solution to identify:

High-risk borrower groups

Changes in default trends

High/low income segments

Loan performance across demographics

Credit score–wise loan distribution

Financial risk patterns

It helps banks and lenders minimize risk, improve loan approval strategy, and detect potential defaulters early.

## Key Metrics & Insights Displayed
1️⃣ Loan & Default Overview

Loan trends across different loan purposes

Average income based on employment type

Default rate variation by year

Loan distribution by borrower age group

2️⃣ Applicant Demographics

Median loan amount by credit score category

Loan distribution by education, age, and marital status

Loan amount comparison by dependents and mortgage status

3️⃣ Financial Risk Metrics

Year-over-year (YOY) loan amount change

YOY default loan change

Year-to-date (YTD) loan performance by credit score bins and marital status

Income bracket + employment type contribution to total loan amount

## Steps Followed (End-to-End Process)
Step 1: Data Import

Imported loan dataset into Power BI
Verified data types (numeric, text, date)
Checked completeness of demographic fields

Step 2: Data Cleaning (Power Query)

Enabled “Column quality, distribution, profile”
Checked missing and error values
Removed blank/inconsistent records
Converted data types for accurate DAX calculations

Step 3: Data Modeling

Categorized key fields (Credit Score Bins, Age Groups, Loan Purpose)
Created standardized dimensions
Ensured the correct relationship structure
Added hierarchies (Year → Month → Day if applicable)

Step 4: DAX Measures Created

Some examples:
 Total Loan Amount = SUM(Loans[LoanAmount])

 Average Income = AVERAGE(Loans[Income])

 Default Rate (%) = DIVIDE(SUM(Loans[Default]),    COUNTROWS(Loans)) * 100

YOY Loan Change = 
    CALCULATE(
        SUM(Loans[LoanAmount]),
        DATEADD(Loans[Year], -1, YEAR)
    )

Step 5: Dashboard Design

Created three interactive pages:
  Loan Default Overview
  Applicant Demographics & Financial Profile
  Financial Risk Metrics

Used soft color themes and simple visuals

Used area charts, line charts, bar charts, donut charts, and Sankey charts

Highlighted important values using data labels

Applied consistent branding and section headers

## Insights From Dashboard
🔹 Loan Default Trends

Default rate peaked around 2015–2016

Default behavior shows cyclical pattern

High default risk observed in certain credit score segments

🔹 Borrower Demographics

Median loan decreases as credit score improves

Younger borrowers tend to take higher loans

Married borrowers with high credit tend to borrow more

Education background strongly influences loan volume

🔹 Income Behavior

Full-time employees show highest income

Unemployed group has significantly lower income → higher risk

🔹 Financial Risk

YOY default changes show years of high financial instability

Credit score bins show strong correlation with loan amounts

High-income individuals (full-time & self-employed) contribute most to loan amounts

## Dashboard Snapshots
                      ## Loan Default Overview

![Page 1](https://github.com/user-attachments/assets/c3ecdffe-df2f-4b91-969a-fdeb199c65a8)

                  ## Applicant Demographics & Financial Profile

![Page 2](https://github.com/user-attachments/assets/0c099f57-271a-48a5-ae4d-0cdc49802a99)

                      ## Financial Risk Metrics

![Page 3](https://github.com/user-attachments/assets/a8901521-efc6-4f1f-a436-a2800e975c79)


## Conclusion

This end-to-end Power BI project provides a comprehensive analytical view of loan default behavior, borrower demographics, and financial risk metrics.

->It supports financial institutions by helping them:

->Identify risky borrower groups

->Improve credit policies

->Strengthen loan approval strategy

->Detect default patterns early

->Reduce financial risk

This dashboard is highly actionable and supports data-driven lending decisions.



 
