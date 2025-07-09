# 🚗 Dynamic Pricing for Urban Parking (Capstone Project)

This project implements a demand-based dynamic pricing system for urban parking spaces. Using real-time or batch processing with **Pathway**, it adjusts parking rates based on live factors like traffic, occupancy, and vehicle type.

---

## 🛠️ Tech Stack Used

- **Python 3.11+**
- **Pathway** – for real-time data pipeline and processing
- **Pandas** – for data manipulation
- **Bokeh** – for interactive visualizations
- **Google Colab** – development environment
- **GitHub** – version control and publishing

---

## 📊 Project Architecture

```mermaid
flowchart TD
    A[dataset.csv (Raw Parking Data)] --> B[Pathway Engine (Static Input)]
    B --> C[UDF: pricing_logic()]
    C --> D[result_table]
    D --> E[pw.io.csv.write()]
    E --> F[final_output.csv]
    F --> G[Download via Colab]
