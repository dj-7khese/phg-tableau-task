# 📊 PHG - Tableau Developer Exercise

This project contains the Tableau dashboard developed as part of a technical assessment for Pearson Ham Group (PHG), demonstrating expertise in data visualization, dashboard development, and dynamic data interaction.

---

## 🧠 Objective

To analyze and visualize general insurance pricing performance metrics using the provided dataset. The goal was to replicate the style and insights of a reference dashboard (see `Tableau Exercise.pdf`) with a clear, interactive Tableau solution.

---

## 📁 Project Structure

- `PHG_Dashboard.twbx` — Final packaged Tableau workbook.
- `Tableau Exercise Dataset.xlsx` — Source data for visualization.
- `Definitions.docx` — Provided field and metric definitions.
- `README.md` — This documentation.
- 📌 [🗂️ Notion Project Plan](https://www.notion.so/Tableau-Task-PHG-1fae4352bc7e801f879af1a86d7e7e47)

---

## 🛠️ Key Features & Skills Demonstrated

- ✅ Parameter-driven controls (Product selector, Date range)
- ✅ Time-based trend analysis (MKT1, MKT5, and Median Index)
- ✅ KPI summary cards and indexed metrics
- ✅ Dual-axis chart with custom formatting
- ✅ Dynamic table with % change and price metrics
- ✅ Table calculations, filters, and LOD expressions
- ✅ Dashboard layout and formatting best practices

---

## 📊 Dashboard Overview

The dashboard includes:

1. **Indexed Price Movement Chart**  
   - Dual-axis: Bar (Median Price) + Line (MKT1, MKT5, Product)
   - Weekly granularity

2. **Indexed Price Table**  
   - Metrics: MKT1 %, MKT5 %, Product %, Median Price
   - Cleaned formatting with % and currency

---

## 🧩 Tools & Technologies

- Tableau Public Desktop Edition
- Microsoft Excel (for initial data exploration)
- GitHub (version control and documentation)
- Notion (project planning)

---

## 📬 Contact

**Dhaval Khese**  
Tableau Developer | Data Visualization Specialist  
🔗 [LinkedIn](https://www.linkedin.com/in/dhaval-khese/)  
📧 khese.dhaval7@gmail.com

---

> ⚠️ Note: This repository is for technical demonstration purposes only. All data and visuals were developed for assessment use.
---

## 📘 Logic & Calculation Overview

This section outlines the core methodology and technical logic used to develop the Tableau dashboard.

### 🔧 1. Project Setup and Planning
- Created a Notion-based project plan to organize tasks, parameters, and charts.
- Used GitHub for version control and documentation delivery.

### 🧩 2. Parameter Configuration
- **Start Date / End Date** parameters dynamically default to a rolling two-month window.
- **Product Selector**: filters all views to one selected product.
- **Dimension Switchers** (optional): allow user to toggle dimension on charts.

### 📊 3. KPI & Metric Logic
- **MKT1 Change**: Avg % change of top 1 prices weekly, excluding 5% extremes.
- **MKT5 Change**: Similar logic for top 5.
- **Product % Change**: Week-over-week % change.
- **Product Median Price**: Median of selected product per week.

### 📈 4. Trend Chart (Dual Axis)
- Lines for MKT1, MKT5, and Product Index values (normalized to 1.000).
- Bar chart for product median price.
- Synced dual axis (Index and £ scale) with custom color scheme.

### 📑 5. Summary Table (Bottom Section)
- Used INDEX() to dynamically label rows.
- CASE + AVG() used to safely aggregate values without mixing types.
- Weekly columns, formatted as heatmap for % change, and £ for prices.

### ⚙️ 6. Advanced Techniques
- Used LOD expressions where needed.
- Applied WINDOW_AVG and LOOKUP for indexing calculations.
- Clean tooltips, synced axes, and formatted legends for clarity.

### 🧩 7. Final Dashboard Assembly
- Top = Chart | Bottom = Table | Filters on top-right
- Responsive to parameters
- Final polish with consistent fonts, layout, and export formatting.

