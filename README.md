# Procure-2-Pay
Perfect idea — a **README.md** makes your Power BI project look professional on GitHub.
Here’s a clean, no-fluff template you can adapt for your **Vendor-Level Spend & Volume Dashboard**.

---

# Vendor Spend & Volume Dashboard (Power BI)

## 📌 Overview

This Power BI dashboard analyzes **Procure-to-Pay (P2P) invoice data** to evaluate vendor spend and invoice patterns.
The goal is to provide finance and procurement teams with clear visibility into **vendor performance, concentration, and spending trends**.

---

## 📂 Dataset

The dashboard uses two CSV files:

1. **Invoice.csv**

   * InvoiceID
   * VendorID
   * LocationID
   * InvoiceDateID
   * Discount Days / Percent
   * Payment Terms Days
   * Payment Status

2. **Invoice Line Item.csv**

   * InvoiceID
   * ItemID
   * Line Item Quantity
   * Unit Price
   * Invoice Amount (in local and converted currency)
   * Exchange Rate
   * Savings

---

## 📊 Key Insights

### 1. Vendor-Level Spend & Volume

* **Total Spend by Vendor** (sum of all invoice amounts)
* **Number of Invoices per Vendor** (distinct count of invoices)
* **Average Invoice Value** (total spend ÷ invoice count)
* **Top 10 Vendors by Spend** (Pareto view of vendor concentration)
* **Spend Trend Over Time by Vendor** (monthly or quarterly trend using Date table)

---

## ⚙️ Data Model

* `Invoice[InvoiceID]` → `Invoice Line Item[InvoiceID]` (1-to-Many)
* `Invoice[InvoiceDateID]` → `Date[DateID]` (Many-to-1)

---


## 📈 Visuals

* **Bar Chart**: Total Spend by Vendor
* **Column Chart**: Number of Invoices per Vendor
* **Table / Column Chart**: Average Invoice Value
* **Bar Chart (Top N)**: Top 10 Vendors by Spend
* **Line Chart**: Spend Trend by Vendor Over Time

---

## 🚀 Next Steps

* Add **Payment Date** to enable On-Time Payment Rate analysis
* Incorporate **PO & GR data** for 3-way match compliance
* Include **Dispute Tracking** for vendor dispute rate metric
* Build **Composite Vendor Scorecard** (0–100) once more data sources are available

---

## 📌 How to Use

1. Clone this repository
2. Open the `.pbix` file in Power BI Desktop
3. Connect to `Invoice.csv` and `Invoice Line Item.csv`
4. Refresh the dashboard

---

## Screenshot
https://github.com/Coder-Wasim/Procure-2-Pay/blob/main/Spend%20Analysis.png
