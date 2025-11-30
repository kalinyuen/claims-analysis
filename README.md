# Claims Analysis

## Project Description
This project examines healthcare claims data containing provider details, billing information, diagnosis codes, and payer records. Python and pandas are used to conduct exploratory data analysis, perform aggregations, and generate visualizations across three integrated datasets.

## Data Source Information
The analysis is based on three CSV files that represent the structure of a healthcare claim:
- HEADER file – Contains claim-level information, including provider NPIs, service dates, and primary payer details.
- LINE file – Contains service-line–level details such as HCPCS codes, modifiers, units, and charges.
- CODE file – Contains all diagnosis codes (ICD-10) associated with each claim.

## How to Run the Notebook
1. Clone this repository in your local machine or google colab.
2. Ensure the three CSV files are in the same directory as the notebook or uploaded to your environment.
3. Open the Jupyter notebook or Google Colab notebook.
4. Run all cells sequentially from top to bottom.

## Summary of Key Findings
- Provider Billing Patterns: SB Internists submitted the largest number of claims in the dataset (152 total), with SB Surgical Associates following behind at 81 claims.
- Primary Payer Mix: Medicare represents the vast majority of claims, making up roughly 70% of all submissions—far more than the next highest payer, HealthFirst FFS, which accounts for around 13%.
- Common Diagnoses: The ICD-10 code that appears most frequently is J96.01 (Acute respiratory failure with hypoxia), recorded 62 times. The next most common diagnoses are I10 (Essential hypertension) and E78.5 (Hyperlipidemia, unspecified), each occurring 49 times.
- Common Procedures: The HCPCS code billed most often is 99291, representing initial critical care services for the first hour. It appears 68 times—considerably more than other high-volume codes such as 99233 and 99232.
- Charges by Place of Service: Ambulatory Surgery Center claims have the highest average charges (approximately $1,912), whereas Outpatient Hospital claims show the lowest average charges (about $330).

## Required Libraries
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```
