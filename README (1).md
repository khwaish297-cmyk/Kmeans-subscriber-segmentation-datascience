# Data Science: K-Means Clustering to Identify Subscriber Segments in Cable Services

---
**This project examines how a cable TV multi-system operator (MSO) can use household spending patterns to develop more relevant subscriber offers. Using monthly payments for video, internet, and landline phone services, our group compared K-means solutions and selected six segments to guide differentiated bundles and cross-sell recommendations. Demographic profiles helped translate the statistical clusters into marketing opportunities.
**---

## Project Goal

The business objective was to identify subscriber groups that could receive different offers to increase customer value and monthly cash flow. For example, an appropriate high-speed internet upgrade could create an opportunity to grow revenue from an existing subscriber. The analysis therefore considered both statistical separation and whether each segment could support a practical offer.

---

## Data Overview

| Dataset | Description |
| --- | --- |
| `cable2.csv` | Course-provided household data containing monthly payments for three cable services and demographic attributes. |

### Unit of Analysis

- 10,000 subscriber households

### Clustering Variables (for K-means)

- **Video:** Amount paid for cable TV services in the most recent month. The assignment associates higher payments with more channels and services.
- **Internet:** Amount paid for internet service in the most recent month. The assignment associates higher payments with faster speeds.
- **Phone:** Amount paid for landline phone service in the most recent month.

### Demographic Profiling Variables

Used to interpret the segments and inform offer recommendations:

- Age of household head
- Household income
- Household size
- Marital status
- Number of children

---

## Methodology

1. **Descriptive analysis:** Examine spending distributions across video, internet, and phone, including zero payments and high-spend outliers.
2. **Standardization assessment:** Retain the original payment scales to preserve absolute spending differences, acknowledging that higher-variance variables have more influence on the solution.
3. **K-means clustering:** Compare six- through ten-cluster solutions and select six clusters based on the highest pseudo-F statistic in the displayed comparison and their usefulness for differentiated offers.
4. **Demographic profiling:** Examine age, income, and household composition to interpret each cluster alongside its service spending.
5. **Offer development:** Propose segment-specific bundles and identify additional variables, including data usage, subscription tenure, and connected devices, that could improve personalization.

---

## Key Findings

- Six distinct customer segments with different spending patterns
- Premium video customers spent heavily on TV services
- Internet-focused customers spent less on video and phone
- Segment differences informed recommendations for premium bundles, internet upgrades, and basic packages

---

## Key Methods & Tools

| Category | Details |
| --- | --- |
| Methods | K-means clustering, Exploratory Data Analysis, Demographic profiling|
| Tools | RStudio (packages: tidyverse, dplyr, stats, ggplot2)|
---

## How to Run

This version documents the analysis and findings from the group presentation. The original R scripts and `cable2.csv` dataset are not included, so the analysis cannot yet be rerun from this repository.

Reproducible setup instructions can be added when the original scripts and a shareable dataset are available.
