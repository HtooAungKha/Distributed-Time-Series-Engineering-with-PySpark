# Distributed Time-Series Engineering with PySpark  
## Window-Based Telemetry Processing on 100K+ Health Records

---

## Overview

This project implements a distributed time-series analytics pipeline using **Apache Spark (PySpark)** to process and transform 100,000+ daily wearable fitness records across 286 users.

The objective is to engineer scalable, partition-aware time-series transformations using:

- Window functions
- Rolling aggregations
- Lag/lead modeling
- Event-based feature engineering
- Multi-level aggregation layers

This project focuses strictly on **data engineering techniques**, not machine learning.

---

## 🗂 Dataset Summary

- **100,000+ records**
- **286 users**
- **13 months of daily telemetry**
- **39 columns**
- Sleep, recovery, strain, HRV, resting heart rate
- Workout event data
- Physiological baselines (HRV baseline, RHR baseline)

The dataset simulates wearable device telemetry for a health analytics platform.

---

## 🏗 Architecture Design

The pipeline follows a layered transformation model:

### Bronze Layer
- Raw CSV ingestion
- Schema inference and type casting
- Date normalization

### Silver Layer
- Partitioned user-level time-series framework
- Rolling metrics (7-day, 30-day)
- Lag/lead event modeling
- Baseline deviation computation

### Gold Layer
- Weekly aggregation
- Streak detection
- Ranking frameworks
- User-level summaries

---

