# AI-Driven Regulatory Genomics Analysis of Lung Cancer

## Overview
This project investigates how chromatin accessibility relates to gene expression in lung cancer cells by integrating ATAC-seq and microarray data. The focus is on understanding regulatory patterns and evaluating whether accessibility-derived features can explain transcriptional activity.

---

## Objective
- Build gene-level regulatory features from ATAC-seq data  
- Integrate chromatin accessibility with gene expression  
- Evaluate relationships using interpretable machine learning  

---

## Approach

### Data Processing
- Parsed gene expression data and mapped probes to gene symbols  
- Aggregated probe-level data into gene-level expression  

### Feature Engineering
- Mapped ATAC-seq peaks to genes using a ±50 kb window  
- Computed accessibility features at the gene level  
- Separated peaks into:
  - Promoter regions (≤ 2 kb from TSS)  
  - Distal regions (> 2 kb)  

### Modeling
- Trained a Random Forest classifier to predict high vs low expression  
- Analyzed feature importance to interpret regulatory signals  

---

## Results

- Weak global association between accessibility and expression  
  - r ≈ 0.12  

- Stronger promoter signal  
  - Promoter r ≈ 0.24–0.27  
  - Distal r ≈ 0.08  

- Model performance  
  - ROC-AUC ≈ 0.73–0.74  

- Promoter features dominate predictive importance  

---

## Key Insight

Promoter-proximal chromatin accessibility shows a stronger relationship with gene expression than distal regulatory regions in this dataset.

---

## Data

- ATAC-seq peaks (GEO / ENCODE, A549 cell line)  
- Gene expression (GEO microarray dataset)  
- Gene annotation (GENCODE)  

---
## Limitations

- ±50 kb window is a simplified approximation of regulatory interactions  
- Microarray data has lower resolution than RNA-seq  
- Analysis is based on a single cell line  

---

## Future Work

- Integrate transcription factor or ChIP-seq data  
- Use RNA-seq for improved expression measurement  
- Extend analysis across multiple datasets  

---

## Technologies


- Python (pandas, numpy)
- PyRanges
- scikit-learn
- matplotlib







