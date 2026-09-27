# Marketing Analytics: K-Means Customer Segmentation for Cable Service Offers

This project examines how a cable TV multi-system operator (MSO) can use household spending patterns to develop more relevant subscriber offers. Using monthly payments for video, internet, and landline phone services, our group compared K-means solutions and selected six segments to guide differentiated bundles and cross-sell recommendations. Demographic profiles helped translate the statistical clusters into marketing opportunities.

Completed for Northwestern University's **IMC460: Data Science**. Group members: Ina Lin, Cindy Chou, Khwaish Gohil, Yin Zhi, and Priya Thakore.

---

## Project Motivation

The business objective was to identify subscriber groups that could receive different offers to increase customer value and monthly cash flow. For example, an appropriate high-speed internet upgrade could create an opportunity to grow revenue from an existing subscriber. The analysis therefore considered both statistical separation and whether each segment could support a practical offer.

---

## Data Overview

| Dataset | Description |
| --- | --- |
| `cable2.csv` | Course-provided household data containing monthly payments for three cable services and demographic attributes. |

### Unit of Analysis

- One subscriber household.
- The assignment describes a source dataset of **10,000 households**.
- The selected model output in our presentation contains **9,780 households**. The presentation does not document the reason for this difference.

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

- **Six clusters explained approximately 74.2% of spending variation.** The selected solution reported a pseudo-F statistic of 5,634.7, the highest among the six- through ten-cluster solutions shown in the presentation.
- **Premium video households were distinct from internet-led households.** Cluster 1 averaged $145.70 in monthly video spending, compared with $28.47 for cluster 2. Cluster 2 had the highest mean internet payment at $46.65.
- **The largest segment combined moderate video and internet spending.** Cluster 5 contained 4,036 households, approximately 41% of the analyzed sample, and supported a family-bundle or internet-upgrade offer hypothesis.
- **Older, video-focused households suggested a different offer approach.** Cluster 3 had an average age of 62.3 and very low internet spending, informing the proposed affordable "Stay Connected" package.
- **Low-spend households supported an essentials-package hypothesis.** Cluster 6 had relatively low payments across all three services, suggesting a basic bundle worth testing.

These offers were recommendations from the case study. Campaign conversion, retention, and revenue impact were not measured. Segment interpretations follow the selected six-cluster output; later slides contain inconsistent cluster references.

---

## Key Methods & Tools

| Category | Details |
| --- | --- |
| Methods | K-means clustering, descriptive statistics, scale assessment, pseudo-F comparison, demographic profiling, offer development |
| Tools | R / RStudio, as identified in the accompanying project description; individual package dependencies are not verified without the original scripts. |
| Deliverable | Group presentation connecting customer segments with proposed service bundles and personalization opportunities. |

---

## How to Run

This version documents the analysis and findings from the group presentation. The original R scripts and `cable2.csv` dataset are not included, so the analysis cannot yet be rerun from this repository.

Reproducible setup instructions can be added when the original scripts and a shareable dataset are available.
