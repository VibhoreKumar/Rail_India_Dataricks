# 🚆 RailVista — Indian Railways Operational Analytics Dashboard

**Turning historical railway data into meaningful operational insights.**

[![Live Dashboard](https://img.shields.io/badge/Live%20Dashboard-Visit%20RailVista-16a34a?style=for-the-badge)](https://railindiadashboard.vercel.app)

RailVista is an interactive analytics dashboard designed to explore historical Indian Railways operational data. It consumes analytics-ready Gold-layer datasets generated through the **RailPulse India Data Engineering pipeline** built using Databricks, PySpark, and Delta Lake.

The dashboard helps users explore train performance, station activity, historical trends, and data quality through a centralized interface.

🔗 **Live Demo:** https://railindiadashboard.vercel.app

---

## 📌 Project Overview

RailVista serves as the visualization and analytical consumption layer of RailPulse India.

The underlying Data Engineering pipeline transforms raw railway CSV datasets through the Medallion Architecture:

- **Bronze:** Raw data ingestion.
- **Silver:** Data cleaning, validation, and transformation.
- **Gold:** Structured, analytics-ready datasets.

RailVista consumes the Gold-layer JSON exports to present historical operational information through interactive visualizations and analytical views.

## 🎯 Dashboard Modules

The dashboard is organized into six major sections.

### 1. Executive Overview
- High-level railway statistics.
- Train and station summaries.
- Key performance indicators based on available Gold datasets.
- Centralized overview of historical data.

### 2. Train Performance Analytics
- Train-wise operational analysis.
- Train performance comparisons.
- Train-level rankings where supported by the data.
- Searchable train information.

### 3. Station Performance Analytics
- Station-wise operational analysis.
- Station activity and observation summaries.
- Station-level comparisons.
- Searchable station information.

### 4. Historical Trend Analysis
- Monthly performance analysis.
- Yearly performance comparisons.
- Historical operational trends.
- Time-based data exploration.

### 5. Data Quality & Source Monitoring
- Gold JSON source validation.
- Dataset availability monitoring.
- Schema and record inspection.
- Loading and error-state visibility.

### 6. Data Lineage & Pipeline Insights
- Overview of the Medallion Architecture.
- Bronze → Silver → Gold data flow.
- Gold dataset source tracking.
- Dataset-level information and availability.

---

## 🏗️ Data Architecture

```text
          Historical Railway CSV Files
                     |
                     v
             Data Ingestion
                     |
                     v
              BRONZE LAYER
              Raw Delta Tables
                     |
                     v
              SILVER LAYER
       Cleaning & Data Validation
                     |
                     v
               GOLD LAYER
        Analytics-Ready Delta Tables
                     |
                     v
             JSON Data Exports
                     |
                     v
              RAILVISTA
          Analytics Dashboard
                     |
          +----------+----------+
          |                     |
          v                     v
    Train Analytics       Station Analytics
          |                     |
          +----------+----------+
                     |
                     v
           Historical Insights
```

## 📂 Gold Data Sources

RailVista uses six Gold-layer JSON exports:

| Dataset | Purpose |
|---|---|
| `overall_kpis.json` | Overall railway statistics |
| `train_performance.json` | Train-level analytics |
| `station_performance.json` | Station-level analytics |
| `station_recovery.json` | Station recovery export data |
| `monthly_performance.json` | Monthly historical analysis |
| `yearly_performance.json` | Yearly historical analysis |

These files are the dashboard's data sources. Metrics and visualizations depend on the fields and records available in the exports.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Dashboard structure |
| CSS3 | Styling and responsive design |
| JavaScript | Dashboard functionality and data processing |
| JSON | Gold-layer data consumption |
| Databricks | Data engineering platform |
| PySpark | Distributed data processing |
| Delta Lake | Reliable data storage |
| Medallion Architecture | Data organization and transformation |
| Power BI | Additional dashboard development (in progress) |

## ✨ Key Features

- Graphite-themed dashboard interface.
- Interactive train and station analytics.
- Monthly and yearly historical analysis.
- Data source monitoring.
- Gold dataset validation and inspection.
- Search and filtering capabilities where supported.
- Data export capabilities.
- Responsive dashboard layout.
- Frontend-only architecture with static JSON data sources.

## 📁 Project Structure

```text
RailVista/
│
├── index.html
│
├── data/
│   ├── overall_kpis.json
│   ├── train_performance.json
│   ├── station_performance.json
│   ├── station_recovery.json
│   ├── monthly_performance.json
│   └── yearly_performance.json
│
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- A modern web browser.
- Python 3 installed (for running a local HTTP server).
- The six Gold JSON files.

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

### 2. Navigate to the project directory

```bash
cd RailVista
```

### 3. Start a local server

```bash
python3 -m http.server 8000
```

### 4. Open the dashboard

Visit:

```text
http://localhost:8000
```

**Note:** Keep the `data` directory alongside `index.html` so the dashboard can fetch the JSON files correctly. Opening the HTML file directly using `file://` may prevent local JSON fetching.

## 📊 Project Data

The project works with historical Indian Railways operational datasets.

The Data Engineering pipeline processes the source records and produces structured Gold-layer datasets for downstream analytics.

The dashboard is intended for **historical analysis and decision support**, not real-time train tracking, ticket booking, or live railway operations.

All displayed metrics should be derived from the available source data rather than manually generated values.

## 🔮 Future Enhancements

- Complete Power BI dashboard integration.
- Enhanced train and station comparison.
- Interactive data dictionary and schema explorer.
- More detailed data lineage visualization.
- Advanced data profiling and quality monitoring.
- Improved analytical reporting and export options.

## 👨‍💻 Author

**Vibhore Kumar**

B.Tech Computer Science Engineering

Interested in Data Engineering, Big Data Processing, and Analytics.

- **Portfolio:** https://vibhorekumar-portfolio.vercel.app/
- **LinkedIn:** [Add your LinkedIn profile URL]
- **GitHub:** https://github.com/VibhoreKumar

---

## ⭐ Support

If you find this project interesting, consider giving the repository a ⭐ on GitHub.

**From Raw Data to Delta Tables to Real Insights.**

*RailVista — Exploring Indian Railways through Data.* 🚆
