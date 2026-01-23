# Aadhaar Operational Audit: Spatiotemporal Volatility & Demographic Displacement

## Project Overview

The Aadhaar ecosystem has transitioned from mass enrollment to a complex **Maintenance Lifecycle**. This project implements a multi-pillar operational audit to identify **Spatiotemporal Volatility**—service demand that is neither uniform over time nor geography—creating localized friction points that aggregate reporting often fails to capture.

## The Three Pillars of Analysis

**Temporal Volatility**: Identifying recurring “skyscraper” surges where daily volume breaches 2.06×–4.68× the mid-week median.

**Spatial Stress**: Mapping **absolute saturation** in districts where workload per service neighborhood materially exceeds the national baseline.

**Demographic Displacement**: Quantifying the **inclusion gap** where adult updates crowd out mandatory, time-sensitive youth biometric maintenance.

## Methodology

The analytical pipeline is structured into five phases to ensure data integrity and systemic validation.

**Phase I — Ingestion & Relational Integration**
Consolidated enrolment, demographic, and biometric streams using memory-optimized loading and correlated activity via a composite geographic key (State–District–Pincode).

**Phase II — Categorical Sanitization**
Standardized state labels by collapsing variants into official State/UT names and corrected administrative drift (e.g., cities misclassified as states).

**Phase III — Temporal Contextualization & Baselining**
Casted timestamps to `datetime64[ns]` to derive cyclical features and established a nominal capacity baseline using stable mid-week medians.

**Phase IV — Operational Metric Synthesis**
Engineered a **Saturation Quotient (Sq)** as a density proxy for infrastructure burden and a normalized **Displacement Score** (0–1) to rank youth exclusion risk.

**Phase V — Statistical Validation & Visualization**
Applied Pareto analysis to identify the vital few states driving throughput and validated relationships via correlation analysis and density profiling.

## Repository Structure

- **Notebooks 1–3**: Cleaning and standardization.
- **Notebooks 4–6**: EDA and Pareto discovery.
- **Notebook 7**: Feature engineering (Sq, load factors, normalization).
- **Notebook 8**: Statistical validation and profiling.
- **Notebook 9**: Spatiotemporal visual synthesis.
- **Analysis Report**: [UIDAI-Data-Hackathon-2026-Analysis-Report](UIDAI-Data-Hackathon-2026-Analysis-Report.pdf)

## Key Findings

1. **The Skyscraper Effect**: Predictable Tuesday and Saturday surges breach nominal capacity following weekend backlog accumulation.
2. **Infrastructure Saturation**: Throughput is highly concentrated; a small set of states process the majority of national volume, with crisis districts operating near historical ceilings.
3. **Operation Sinks**: Districts with high adult update dominance exhibit measurable crowding-out of youth biometric maintenance.

## Technical Stack

Python (Pandas, NumPy); Visualization (Matplotlib, Seaborn); Statistics (SciPy).

## Authors

Ankitha Hathwar T N  
Priyangshu Mukherjee
