# UK EPC Parquet Converter 🏠⚡

A memory-efficient Python utility designed to convert the massive **UK Domestic Energy Performance Certificate (EPC)** dataset from its raw ZIP/CSV format into a highly compressed **Parquet** file.

## 🚀 Why this project?
The UK Domestic EPC dataset is roughly **5.9GB** in its compressed ZIP form and contains over **25 million rows** spread across **347 regional CSVs**. 

This script solves two major problems:
1. **Memory Limits:** Processes data region-by-region to prevent `MemoryError` on standard laptops.
2. **BI Optimization:** Converts messy CSVs into **Parquet (Snappy)**, which is ~80% smaller and loads significantly faster in **Qlik Sense**, **Power BI**, and **Python**.

## 🛠️ Requirements
* **Python 3.10+**
* **Polars:** The high-performance data engine.
* **PyArrow:** For Parquet file support.

## 💻 Installation & Usage
1. Clone this repository.
2. Install the dependencies:
   ```bash
   python -m pip install polars pyarrow
3. Place your all-domestic-certificates.zip from the EPC Open Data Service into the project folder.
   
4.Run the converter :
   python convert.py
