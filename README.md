# 💳 Credit Card Fraud & Risk Detection Pipeline

This project implements a fraud and risk detection data pipeline using **Apache Airflow**, **Apache Spark**, and **BigQuery**, built to automate and scale the processing of transaction and cardholder data.

---

## 📦 Project Structure

```
Credit-Card-Fraud-and-Risk-Pipeline/
├── airflow_job.py                 # Airflow DAG to orchestrate the pipeline
├── spark_job.py                   # Spark job to process and classify transactions
├── cardholders.csv                # Cardholder metadata
├── transactions_*.json            # Daily transaction files
├── test_transactions_processing.py # Unit tests for Spark logic
├── requirements.txt               # Python dependencies
└── README.md                      # Project documentation
```

---

## ⚙️ Pipeline Overview

1. **Data Ingestion**  
   Airflow loads JSON transaction files and cardholder data into the pipeline.

2. **Processing with Spark**  
   Spark transforms, cleans, and flags risky transactions using rules or ML models.

3. **Validation & Testing**  
   PySpark transformations are unit-tested using `test_transactions_processing.py`.

4. **Orchestration**  
   Airflow coordinates ingestion, processing, and validation as DAG tasks.

---

## 🚀 Technologies Used

- **Apache Airflow** – Task orchestration  
- **Apache Spark (PySpark)** – Distributed data processing  
- **BigQuery (optional)** – For storing curated risk data  
- **GCS / Local Files** – As data sources  
- **Python 3.11** – Runtime  
- **Pytest** – Test framework

---

## 🧪 Input Files

- `cardholders.csv` – Contains cardholder info like name, region, account status  
- `transactions_*.json` – Daily transaction logs with metadata and amount  

---

## ✅ DAG Highlights

| Task                          | Description                          |
|------------------------------|--------------------------------------|
| `start_pipeline`             | Dummy start                          |
| `load_cardholder_data`       | Loads `cardholders.csv`              |
| `load_transaction_data`      | Loads daily JSON files               |
| `process_transactions`       | Applies Spark transformations        |
| `run_tests`                  | Executes PySpark test suite          |
| `end_pipeline`               | Dummy end                            |

---

## 🧠 Risk Detection Logic

The Spark job detects high-risk transactions by:
- Filtering suspicious amounts or geolocations
- Flagging blacklisted cardholders
- Enforcing account limits or fraud thresholds

---

## 📜 Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
```

---

## 🧑‍💻 Author

**Niranjana Subramanian**  
_Data Engineer | Data Pipeline Automation Enthusiast_
