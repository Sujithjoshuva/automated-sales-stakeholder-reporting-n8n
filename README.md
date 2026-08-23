# Automated Sales Stakeholder Reporting System using n8n

## Project Overview

This project automates the process of generating and sending sales performance updates to stakeholders.

A user uploads a sales CSV dataset through an n8n form. The workflow processes the dataset, converts the required fields into numeric values, calculates profit margins, summarizes key business metrics, generates a stakeholder report, and automatically sends the report through Gmail.

---

## Problem Statement

Preparing stakeholder updates manually can involve repetitive work:

- Reading and processing CSV files
- Calculating business metrics
- Calculating profit margins
- Summarizing sales performance
- Writing stakeholder updates
- Sending reports through email

The goal of this project is to automate this process using n8n.

---

## Solution

The workflow:

1. Receives an uploaded CSV dataset through an n8n form
2. Extracts data from the CSV file
3. Converts Sales, Profit, and Units to numeric values
4. Calculates profit margin for each record
5. Calculates total sales, total profit, and total units sold
6. Calculates overall profit margin
7. Generates a stakeholder report dynamically
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

The workflow processes a sales CSV dataset containing:

| Column | Description |
|---|---|
| Date | Date of the sales record |
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

Sum of sales across all uploaded records.

### Total Profit

Sum of profit across all uploaded records.

### Total Units Sold

Sum of units across all uploaded records.

### Overall Profit Margin

```text
Overall Profit Margin = (Total Profit / Total Sales) × 100
```

---

## Technologies Used

- n8n Cloud
- n8n Form Trigger
- CSV
- JSON
- n8n Expressions
- Edit Fields
- Extract From File
- Summarize
- Gmail

---

## Workflow Features

- CSV file upload
- Automated data extraction
- Numeric data conversion
- Row-level KPI calculation
- Dataset-level KPI aggregation
- Dynamic stakeholder report generation
- Automated Gmail delivery

---

## Learning Progress

### Lesson 1: n8n Fundamentals

- Workflows
- Nodes
- Items
- JSON
- Expressions
- Dynamic values
- Calculations

### Lesson 2: CSV Dataset Processing

- Form-based file upload
- Binary data
- Extracting CSV data
- Converting text values to numbers
- Row-level profit margin calculation
- Dataset-level aggregation

### Lesson 3: Automated Stakeholder Reporting

- KPI summarization
- Overall profit margin calculation
- Dynamic report generation
- Gmail integration
- End-to-end workflow testing

---

## Project Status

Version 1 is complete and was successfully tested end-to-end.

The workflow successfully:

- Accepted a CSV upload
- Processed the dataset
- Calculated business KPIs
- Generated a stakeholder report
- Sent the report through Gmail
- Delivered the email successfully

---

## Future Improvements

- Regional sales analysis
- Product performance analysis
- HTML email formatting
- Error handling
- Scheduled reporting
- Additional business KPIs
