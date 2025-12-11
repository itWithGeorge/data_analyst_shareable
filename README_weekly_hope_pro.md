# 🎰 Weekly Hope — Automated Lottery Analytics & Prediction Pipeline

[![Made with BigQuery](https://img.shields.io/badge/Powered%20by-BigQuery-4285F4.svg)](#)
[![Google Cloud Functions](https://img.shields.io/badge/Cloud%20Functions-Node.js-34a853.svg)](#)
[![Apps Script](https://img.shields.io/badge/Automation-Apps%20Script-fbbc05.svg)](#)
[![Slack Bot](https://img.shields.io/badge/Output-Slack-4A154B.svg)](#)

---

## 📄 Arhitecture (PDF)
**View the architecture:** 👉 [REPORT](./weekly_hope_architecture.pdf)

---

## 📝 Description

**Weekly Hope** is a fully automated **data engineering + analytics workflow** that ingests lottery results from 1957 onward, enriches them with weekly scraped updates, runs statistical models in **BigQuery**, and sends a formatted **weekly prediction message to Slack**.

The project demonstrates how a lightweight, event-driven pipeline can combine **ETL**, **analytics**, and **automated reporting** using Google Cloud’s serverless stack.

---

## 🎯 Scope Highlights

- **Historical Data Load:** Official Excel export (1950s → today) ingested into BigQuery as the canonical dataset.  
- **Incremental Weekly Updates:** A scheduled scraper retrieves the newest winning numbers and writes them to Google Sheets.  
- **Apps Script Trigger:** Sheet changes trigger Apps Script, inserting *only the latest draw* into BigQuery.  
- **BigQuery Analytics:** A scheduled SQL job computes the weekly recommended 5 numbers using:
  - statistical frequency functions,  
  - distribution analysis,  
  - and controlled randomness.  
- **Prediction View:** Results are published into a dedicated BigQuery view for consumption.  
- **Slack Delivery:** A Node.js Cloud Function (triggered by Cloud Scheduler) queries the view, formats the message, and posts it to Slack every week.

---

## 🚀 End-to-End Flow

1. **Historical Excel** → Imported once into BigQuery (`lotto_historical_draws`).  
2. **Weekly scraper** → Writes newest draw to **Google Sheets**.  
3. **Apps Script** → Detects update → Appends record to BigQuery.  
4. **BigQuery scheduled query** → Produces weekly “recommended 5 numbers” dataset/view.  
5. **Cloud Scheduler → Cloud Function** → Fetch prediction → Push to **Slack**.  

This forms a clean, maintainable **ETL → Analytics → Notification** pipeline with no manual steps.

---

## 📊 Featured Components

### **BigQuery Analytics**
- Frequency analysis of past draws  
- Weighted randomness for non-deterministic variety  
- Scheduled SQL logic generating a *single recommendation per week*

### **Slack Output**
- Cloud Function returns:
  - recommended numbers,  
  - period context,  
  - optional statistics (e.g., top frequencies)  
- Delivered as a nicely formatted Slack message

### **Google Sheets + Apps Script**
- Lightweight ingestion layer  
- Zero-ops: triggers automatically on sheet change  
- Ensures only the **newest weekly row** is added to BigQuery

---

## 🔧 Technologies Used
- **Google BigQuery** (data warehouse, scheduled queries, analytical SQL)  
- **Google Apps Script** (event-driven ingestion)  
- **Google Sheets** (staging layer for scraped data)  
- **Node.js Cloud Functions** (Slack message automation)  
- **Cloud Scheduler** (cron-like triggers)  
- **Slack Incoming Webhooks** (report delivery)

---

## 📬 Contact
For questions or collaboration, feel free to reach out via email/LinkedIn.
