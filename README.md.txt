# Automated Sales Stakeholder Reporting System using n8n

## Project Overview

This project automates the process of generating and sending sales performance updates to stakeholders.

A user uploads a sales CSV dataset through an n8n form. The workflow processes the dataset, converts the required fields into numeric values, calculates profit margins, summarizes key business metrics, generates a stakeholder report, and automatically sends the report through Gmail.

This project is being developed as part of learning n8n workflow automation, data processing, and business reporting.

---

## Problem Statement

Preparing stakeholder updates manually can require repetitive work such as:

- Collecting a sales dataset
- Reading and processing CSV files
- Calculating business metrics
- Calculating profit margins
- Summarizing sales performance
- Writing a stakeholder update
- Sending the report through email

The goal of this project is to automate this workflow using n8n.

---

## Solution

The automated workflow:

1. Receives an uploaded CSV dataset
2. Extracts data from the CSV file
3. Converts numeric fields into numbers
4. Calculates profit margin for each record
5. Aggregates total sales, profit, and units sold
6. Calculates the overall profit margin
7. Generates a stakeholder report
8. Sends the report automatically through Gmail

---

## Workflow Architecture

```text
On Form Submission
        ↓
Extract From File
        ↓
Convert Data Types
        ↓
Calculate Row-Level Profit Margin
        ↓
Summarize KPIs
        ↓
Calculate Overall Profit Margin
        ↓
Format Stakeholder Report
        ↓
Gmail - Send Message
```

---

## Dataset

The workflow uses a sales CSV dataset with the following fields:

| Column | Description |
|---|---|
| Date | Date of the sales transaction |
| Region | Sales region |
| Product | Product sold |
| Sales | Sales amount |
| Profit | Profit amount |
| Units | Number of units sold |

---

## Business Metrics

### Row-Level Profit Margin

```text
Profit Margin = (Profit / Sales) × 100
```

### Total Sales

Total sales value across all records.

### Total Profit

Total profit across all records.

### Total Units Sold

Total number of units sold across all records.

### Overall Profit Margin

```text
Overall Profit Margin = (Total Profit / Total Sales) × 100
```

---

## Technologies Used

- n8n Cloud
- n8n Form
- CSV
- JSON
- n8n Expressions
- Edit Fields
- Extract From File
- Summarize
- Gmail

---

## Learning Progress

### Lesson 1: n8n Fundamentals

- Understanding workflows
- Understanding nodes
- Understanding items
- Working with JSON
- Using expressions
- Accessing dynamic data
- Performing calculations

### Lesson 2: Uploading and Processing a CSV Dataset

- Creating an n8n form
- Uploading a CSV dataset
- Understanding binary data
- Extracting data from a CSV file
- Converting text values to numbers
- Calculating row-level profit margins

### Lesson 3: Automated Stakeholder Reporting

- Aggregating business metrics
- Using the Summarize node
- Calculating total sales
- Calculating total profit
- Calculating total units sold
- Calculating overall profit margin
- Creating a dynamic stakeholder report
- Integrating Gmail
- Sending automated email reports

---

## Project Status

Version 1 is complete and has been successfully tested end-to-end.

The workflow successfully:

- Accepted a CSV upload
- Processed the dataset
- Calculated the required KPIs
- Generated a stakeholder report
- Sent the report through Gmail
- Delivered the email successfully

---

## Future Improvements

- Regional sales analysis
- Product performance analysis
- Better stakeholder report formatting
- Automated error handling
- Scheduled reports
- Additional business KPIs