# Descriptive Project Title i.e. "Cafe Financial Analysis & Insights"

## Project Overview

Our team was hired by the owner of a popular café chain to clean and explore their transaction data in preparation for new marketing initiatives. The dataset was initially messy and inconsistent, making analysis difficult. Our goal was to identify peak sales periods, explore general sales trends, and ensure the data's reliability to provide clear, actionable recommendations for the business.Identify peak sales periods, explore general sales trends, and ensure the data's reliability to provide clear, actionable recommendations for the business.
## Business Questions
- What are the peak sales months?
- Are weekends busier than weekdays?
- Any other findings stand out and relevant to the stakeholders?
- How reliable was the data?  What cleaning was needed?

## Data Cleaning Summary
- Data type corrections made
- Missing data handling strategy
- Duplicate handling
- Any columns dropped or imputed (and why)

### Excel
- Cleaning done by Ro

<p align="center">
To make the cleaning process easier, I first created a live Missing Value Tracker. I used COUNTBLANK functions for every column to count missing cells, and used conditional formatting to display green if there are no blanks, or red if there are blanks.
</p>

![](README-files/Excel-Live-Tracker.png)

<p align="center">
Once I had a live tracker, I began cleaning the data.
</p> 

Key actions include: 

- converting all UNKNOWN and ERROR rows to blanks.
- Filling in empty rows for Item, Quantity, Price Per Unit, and Total Spent through mathematical functions.
- Filling in 20 missing rows for the Total Spent column using the average value of Total Spent per each Item, which allows me to fill in Quantity.
- Dropping 5 rows due to missing Item and Price Per Unit values.

<p align="center">
This allowed me to clear up much of the missing rows, leaving only Transaction Date, Location, and Payment Method to deal with.
</p>

![](README-files/Excel-Live-Tracker4.png)

1. Convert ERROR and UNKNOWN entries for all rows to blanks by filtering each column and replacing them with " ".									
2. Filtered Items Column to blank, filtered PPU Column to $1, $1.5, $2, & $5 respectively and filled filtered rows with IF functions to match items with PPU.									
3. Filtered PPU Column to blank, Filtered Items Column to each item to fill filtered rows with IF functions to match PPU with items.									
4. Filtered QTY Column and PPU Column to remove blanks, changed Total Spent Row to functions for those filtered rows.									
5. Filtered Total Spent Column and QTY Column to remove blanks, Filtered PPU Column to blanks, changed to functions for those filtered rows. --> prevents function overlap.									
6. Filtered Total Spent Column and PPU Column to remove blanks, Filtered QTY Column to blanks, changed to functions for those filtered rows. --> prevents function overlap.									
7. Dropped rows 1763, 2291, 3781, 4154, 7599 due to no Item name, PPU.									
8. Filled the 20 missing rows for Total Spent with Average Total Spent, for each matching Item, marked with orange									
9. Filled Transaction Date, Location, and Payment Method Columns with UNKNOWN using search and filter for filtered range



## Key Findings
- Summary stats (mean, median, etc.)
- Insights from trends by month/day
- Additional analysis looked at
- Any bonus feature engineering

## Reflections
- Challenges we faced
- Any biases
- What we would do differently next time

## Takeaways & Recommendations
- What can you tell the cafe owner and why should they care

## Folder Structure (EXAMPLE ONLY)
```text
.
├── data/
│   ├── raw/
│   └── cleaned/
├── excel/
│   ├── analysis_workbook.xlsx
│   └── cleaning_template.xlsx
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda_insights.ipynb
│   └── README.md
