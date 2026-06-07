# Foodrush Invoice Automation

Automated generation of styled Excel reports and professional PDF invoices for a food delivery platform.  
Reduced manual invoice processing from 3 days to 10 minutes.

## Problem
Our accounts team used to manually create 200+ restaurant invoices each month from raw order dumps.  
This took 2-3 days, was error‑prone, and prevented the team from focusing on analysis.

## Solution
A Python pipeline built in Google Colab that:
- Reads Excel order data, cleans it, and groups restaurant branches (e.g., "Sadia's Kitchen (All Branches)").
- Applies custom pricing rules (e.g., exclude orders below 250 Tk for Gapush Gupush).
- Generates:
  - A styled Excel file with separate sheets per restaurant (A4 ready).
  - Professional PDF invoices with pink `bKash`, blue email, and signatures.
  - A 3‑page operational report with tables and charts.

## Tech Stack
- Python
- pandas, numpy
- fpdf2 (PDF generation)
- openpyxl (Excel styling)
- matplotlib (charts)
- num2words (amount in words)

## How to Use
1. Open the notebook in Google Colab.
2. Upload your order Excel file (must follow the expected format).
3. Upload `address.csv` and `remark.csv` (templates provided in `/sample_data`).
4. Run all cells – outputs: `restaurant_orders_styled.xlsx`, `All_Invoices_Automatic.pdf`, `Foodrush_Operational_Report.pdf`.

> **Note**: This notebook is designed for internal use at Foodrush. You may need to adapt column names and pricing rules for your own data.

## Sample Outputs
![Invoice sample](sample_output/invoice_sample.png)  
![Report sample](sample_output/report_sample.png)

## License
MIT
