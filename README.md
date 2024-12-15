# Project: End-to-End ETL Pipeline with GCP Cloud Storage, BigQuery, and Looker Studio

## Overview
This project demonstrates a complete **ETL (Extract, Transform, Load)** pipeline leveraging Google Cloud Platform (GCP) services to process and analyze data. The pipeline extracts data stored in GCP Cloud Storage, processes it using **Mage** for ETL, transforms the data into **dimension** and **fact tables**, and loads it into **BigQuery** for querying. Finally, the processed data is visualized using **Looker Studio**.

## Key Components
1. **GCP Cloud Storage**: Stores the raw CSV data.
2. **Compute Engine**: Virtual machine for running ETL scripts and Mage setup.
3. **Mage**: An open-source tool for orchestrating ETL pipelines.
4. **BigQuery**: Cloud-based data warehouse for storing and querying data.
5. **Looker Studio**: Visualization tool for creating reports and dashboards.

---

## Project Workflow


The following diagram illustrates the ETL pipeline workflow for the Uber Data Analysis project:

![Uber Data Analysis Workflow](https://github.com/praveenreddy82472/DEproject_UberDataAnalysis/blob/main/images/UberFlow%20(1).png)


### 1. Data Dump into GCP Cloud Storage
- Uploaded the raw CSV file(s) into a **GCP Cloud Storage bucket**.
- Ensured proper permissions and bucket configuration for accessibility.

### 2. Setup Google Compute Engine (GCE)
Provisioned a virtual machine on **Google Compute Engine** to host and execute the ETL pipeline.

**Commands to Make System Ready:**
```bash
# Update system packages
sudo apt update && sudo apt upgrade -y

# Install necessary tools
sudo apt install -y python3-pip git

# Install Mage for ETL
pip install mage-ai

# Launch Mage
mage start
