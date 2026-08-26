# Automated Sales Stakeholder Reporting with n8n

This project is an automated sales analysis workflow built using n8n.

The workflow accepts a sales CSV file, processes the data, performs sales analysis, generates performance reports, and sends the results through Gmail.

## Project Features

- Upload a sales CSV file
- Extract data from the CSV file
- Convert Sales, Profit, and Units into numeric values
- Calculate profit margins
- Calculate overall sales KPIs
- Analyze sales performance by region
- Identify the region with the highest sales
- Identify the region with the highest profit
- Identify the region with the highest profit margin
- Generate automated sales reports
- Send reports through Gmail

## Project Structure

```text
automated-sales-stakeholder-reporting-n8n/
│
├── README.md
│
├── workflow/
│   └── regional_sales_analysis_workflow_clean.json
│
└── data/
    └── sales_data.csv
