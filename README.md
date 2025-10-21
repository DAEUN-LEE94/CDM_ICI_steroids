# CDM_ICI_steroids
R code for a multicenter target trial emulation assessing the causal impact of glucocorticoid timing and dose on survival in advanced NSCLC treated with immune checkpoint inhibitors using time-dependent propensity score matching and CDM-based real-world data.

# Impact of Early and High-Dose Glucocorticoids on Survival in Advanced NSCLC Treated with Immune Checkpoint Inhibitors  
### A Multicenter Target Trial Emulation using CDM Data

---

## Overview
This repository contains all files required to reproduce the target trial emulation study evaluating the causal effects of systemic glucocorticoid timing and dose on survival outcomes in advanced non–small cell lung cancer (NSCLC) patients treated with immune checkpoint inhibitors (ICIs).  
Analyses were performed across four Korean tertiary hospitals using the Observational Medical Outcomes Partnership (OMOP) Common Data Model (CDM).

---

## Repository Structure

### 1️⃣ ATLAS Entry Cohort Query Files  
Cohort definition and database-specific queries for reproducible cohort construction in ATLAS.  
- `ATLAS_entry cohort_definition.docx`  
- `ATLAS_entry cohort_JSON.txt`  
- `ATLAS_entry cohort_Oracle.txt`  
- `ATLAS_entry cohort_PostgreSQL.txt`

### 2️⃣ Concept Sets  
Clinical concept definitions used for cohort inclusion/exclusion and covariate construction.  
- `concept sets.docx`

### 3️⃣ Analysis Code (R Markdown)  
R scripts for data extraction, matching, and outcome estimation.  
- `1_ICI_CDM_SQL_Data extraction.Rmd` — Extract CDM-based patient- and treatment-level data  
- `2_ICI_CDM_Data prep_TDPS MATCH.Rmd` — Prepare data and perform time-dependent propensity score (TDPS) matching  
- `3_ICI_CDM_outcome estimation.Rmd` — Estimate survival and treatment effects with Cox models and meta-analysis  

---

## Dependencies
- R ≥ 4.2.0  
- OMOP CDM

---

## Reproducibility
1. Define entry cohort using ATLAS query files.  
2. Extract CDM data according to `concept sets.docx`.  
3. Run R scripts in order:  
   `1_Extraction → 2_Matching → 3_Outcome`.  
4. Outputs include matched cohort data, hazard ratios, and meta-analysis results.

---

## License
This repository is distributed for academic and non-commercial research purposes only.  

---

## Contact
For methodological details or collaboration inquiries, please contact:  
**[Da Eun Lee, Pharm.D/Ph.D]**  
**[College of Pharmacy, Seoul National University, Seoul, Republic of Korea]**  
**[lde090168@gmail.com or ldaeun2@snu.ac.kr]**
