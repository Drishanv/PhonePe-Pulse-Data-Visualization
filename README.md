# 📊 PhonePe Pulse Data Visualization (Power BI Dashboard)

This project is an end-to-end data visualization solution built using **Power BI**, based on the PhonePe Pulse dataset.  
The goal is to transform the raw data extracted from the PhonePe Pulse GitHub repository into **interactive dashboards**, uncovering insights across **India, States, and Districts**.

---

## 📁 Project Structure

The dashboard contains **three pages**, each dedicated to a different level of analysis:

### **1️⃣ Overview & Trends (National Insights)**
- Total Transactions  
- Total Amount  
- Total Users  
- YoY Growth  
- CAGR  
- Top States by Transaction Amount  
- User Device Share (Brand-wise)  
- Year-on-Year Trend (2018–2022)  
- Users vs Transactions Scatter Plot  

### **2️⃣ State-Wise Insights**
- State ATV  
- Multi-Year Growth %  
- State Rank by Amount  
- Transactions per User  
- Quarterly Growth Trend  
- Quarter-wise Transaction Comparison  
- Cumulative Transaction Trend  
- Transaction Breakdown by Type  

### **3️⃣ District Level Analytics**
- Top Districts by Transaction Amount  
- District Yearly Transaction Trend  
- District Performance Matrix (Amount, Users, Transactions)  
- District Engagement Score  
- District Insights Summary (Dynamic: highest district, lowest district, user leader, etc.)

---

## 📸 Dashboard Screenshots

### **Overview & Trends**
![Overview Page](./dashboard-screenshots/Overview%20and%20trends.png)

### **State-Wise Insights**
![State Page](./dashboard-screenshots/State%20level%20insights.png)

### **District-Level Analytics**
![District Page](./dashboard-screenshots/District%20level%20insights.png)

---

## 🧩 Problem Statement
According to the project documentation :contentReference[oaicite:1]{index=1}:

The PhonePe Pulse repository contains extensive data on digital transactions across India.  
The objective is to process, clean, and visualize this data using a live interactive dashboard that:
- Displays key financial and user insights  
- Supports drill-down analysis  
- Provides at least **10 dropdown filters**  
- Helps users explore trends and patterns easily  

---

## 🚀 Features & Highlights

### ✔ Fully Interactive Power BI Dashboard  
- Slicers for Year, Quarter, State, District, and more  
- Drill-down and cross-filtering across visuals  

### ✔ Multi-Level Analysis  
- National level trends  
- State-level KPIs & transaction breakdowns  
- District-level deep insights  

### ✔ Custom Metrics  
- **State ATV**  
- **District Engagement Score**  
- **CAGR**  
- **YoY Growth %**  

### ✔ Insight Box (Dynamic Narrative)  
Automatically displays:
- Highest Transaction District  
- Top User District  
- Lowest Transaction District  
- Highest ATV District  
- Engagement Score  

---

## 🛠 Tools & Technologies
- **Power BI** – Data Visualization  
- **Power Query** – Data Cleaning & Transformation  
- **DAX** – Calculated measures & metrics  
- **JSON Theme** – Custom styling (Purple theme)  
- **PhonePe Pulse Dataset** – Source data  

---

## 🧠 Learning Outcomes
As per the project documentation (page 3) :contentReference[oaicite:3]{index=3}:

- Ability to build interactive dashboards in Power BI  
- Understanding of digital payments ecosystem  
- Skills in trend analysis & KPI development  
- Hands-on experience with cleaning, modeling, and visualizing real datasets  

---

## 🧮 Key DAX Measures Used

```DAX
Total District Amount = SUM(phonepe_district_master[amount])

Total District Transactions = SUM(phonepe_district_master[trans_counts])

Total District Users = SUM(phonepe_district_master[registered_users])

District ATV = DIVIDE([Total District Amount], [Total District Transactions])

Engagement Score = DIVIDE([Total District Transactions], [Total District Users])
