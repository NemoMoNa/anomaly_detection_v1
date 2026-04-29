# Anomaly Detection Mini Project (Baseline)

This repository contains a small hands-on anomaly detection mini project using server metrics data.

The goal of this project was to build a simple and reproducible anomaly detection workflow, including:

- loading time-series server metrics data
- basic feature engineering
- comparing simple baseline methods
- evaluating results with standard metrics
- saving experiment outputs for reproducibility

## Project Scope

This is not a production-ready monitoring system.

It is a learning-oriented, practical mini project created as part of my training toward becoming an AI Engineer. The focus was on building a working baseline and understanding the end-to-end workflow.

## Dataset

Input data:
- `server_metrics.csv` (used locally during development)

Columns used:
- `timestamp`
- `cpu_pct`
- `latency_ms`
- `label`

## Features

The following features were used:
- raw numeric metrics
- first-order difference features (`diff1`)

These were used to create a simple feature set for anomaly detection.

## Models Compared

This project compares two baseline approaches:

1. **Z-score baseline**
2. **Isolation Forest**

## Result Summary

Best model:
- **Isolation Forest**

Metrics from the saved run:
- PR-AUC: **0.7599**
- Precision: **0.8971**
- Recall: **0.6100**
- F1: **0.7262**

## Files in This Repository

- `01_anomaly_detection_minimal.ipynb`  
  Main notebook for the anomaly detection workflow

- `run_cfg.json`  
  Run configuration used for the experiment

- `metrics.json`  
  Saved evaluation metrics

- `train_log.tsv`  
  Output log for the run

- `errors.tsv`  
  Saved false positives / false negatives or top anomaly candidates

## Current Repository Structure

```text
anomaly_detection_v1/
├── 01_anomaly_detection_minimal.ipynb
├── README.md
├── LICENSE
├── .gitignore
├── run_cfg.json
├── metrics.json
├── train_log.tsv
└── errors.tsv
