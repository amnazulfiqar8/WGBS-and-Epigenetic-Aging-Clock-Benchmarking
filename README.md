# 🧬 Epigenetics Analysis Pipeline & Aging Clock Benchmarking

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Galaxy](https://img.shields.io/badge/Galaxy-Workflow-orange.svg)
![Bioinformatics](https://img.shields.io/badge/Field-Bioinformatics-green.svg)
![Status](https://img.shields.io/badge/Status-Complete-success.svg)
![License](https://img.shields.io/badge/License-MIT-lightgrey.svg)

---

# 📌 Project Overview

This repository presents two integrated epigenetics analyses:

## 🔹 1. WGBS DNA Methylation Analysis (Galaxy Workflow)
A complete pipeline for processing Whole Genome Bisulfite Sequencing (WGBS) data.

## 🔹 2. Epigenetic Aging Clock Benchmarking (Python + Biolearn)
A computational benchmarking framework comparing DNA methylation–based aging models.

---

# 🎯 Objectives

- Process raw WGBS sequencing data
- Extract methylation patterns
- Identify Differentially Methylated Regions (DMRs)
- Benchmark epigenetic aging clocks
- Evaluate prediction accuracy
- Visualize biological aging patterns

---

# 🧪 Part 1: WGBS DNA Methylation Analysis (Galaxy)

## 🔬 Workflow Overview

FASTQ → QC → Alignment → Bias Check → Extraction → Visualization → DMR Detection

---

## 📁 Dataset Information

| Sample | Description |
|--------|------------|
| NB | Normal breast |
| BT089 | Fibroadenoma |
| BT126, BT198 | Carcinomas |
| MCF7 | Cell line |

Reference Genome: hg38  
Source: Zenodo (Record 557099)

---

# ⚙️ Pipeline Steps

## 1. Data Upload
Upload FASTQ files into Galaxy using URL or shared data libraries.

---

## 2. Quality Control (Falco)

- High T content and low C content observed
- Due to bisulfite conversion (C → T)
- QC may show "fail" but this is expected

---

## 3. Alignment (bwameth)

- Handles bisulfite conversion
- Standard aligners cannot handle C→T changes
- Output: BAM file

---

## 4. Methylation Bias (MethylDackel)

- CpG methylation ~70–75%
- Slight bias at read ends
- Overall low bias

---

## 5. Methylation Extraction

- Output: BedGraph file with CpG methylation fractions

---

## 6. Visualization

Tools: computeMatrix, plotProfile

Key findings:
- Methylation decreases near TSS
- Indicates promoter hypomethylation

Multi-sample trends:
- MCF7 → highest methylation
- Normal → lowest
- Tumor → intermediate

---

## 7. DMR Detection (Metilene)

- Identifies differentially methylated regions
- Outputs statistical plots and region data

---

# Key Concepts

| Concept | Explanation |
|--------|------------|
| Bisulfite Conversion | C → T |
| CpG Islands | Promoter regions |
| DMR | Differential methylation |
| Bias | Read-end artifacts |

---

# Part 2: Epigenetic Aging Clock Benchmarking

## 📊 Overview

Benchmarking 8 DNA methylation aging clocks using Biolearn.

---

## 📁 Datasets

| Dataset | Samples | CpGs | Age Range |
|--------|--------|------|----------|
| GSE120307 | 34 | 485K | 19–54 |
| GSE41169 | 95 | 485K | 18–65 |

---

## ⏳ Aging Clocks

- Horvath  
- Hannum  
- SkinBloodClock  
- PhenoAge  
- GrimAge  
- DunedinPACE  
- PCHorvath1  
- PCGrimAge  

---

# ⚙️ Workflow

## Install Requirements

pip install biolearn numpy pandas matplotlib scikit-learn scipy

---

## Steps

1. Load datasets using DataLibrary  
2. Load models using ModelGallery  
3. Generate predictions  
4. Perform visualization and evaluation  

---

# 📊 Visualizations

## Correlation Matrix
- Shows agreement between clocks
- Most clocks highly correlated
- DunedinPACE differs

---

## Deviation Heatmap
- Red → biologically older
- Blue → biologically younger

---

## Prediction Plots
- Predicted vs chronological age
- Ideal: diagonal line

---

# 📏 Metrics

| Metric | Meaning |
|------|--------|
| MAE | Average error |
| RMSE | Penalizes large errors |
| Pearson r | Correlation |

---

# 📊 Key Findings

- Horvath clocks perform best
- Strong correlation across models
- Dataset-dependent variation
- DunedinPACE captures different biology

---

# 📂 Repository Structure

Epigenetics-Analysis/
│
├── WGBS_Galaxy/
├── Aging_Clock_Benchmark/
├── README.md
└── requirements.txt

---

# ▶️ How to Run

git clone https://github.com/your-username/your-repo.git  
cd your-repo  
jupyter notebook  

---

# 📦 Requirements

- biolearn  
- numpy  
- pandas  
- matplotlib  
- scikit-learn  
- scipy  

---

# 📚 References

- Horvath (2013)  
- Hannum (2013)  
- Levine (2018)  
- Lu (2019)  
- Belsky (2022)  
- Zhang (2019)  

Biolearn: https://github.com/bio-learn/biolearn  

---

# 🚀 Highlights

- End-to-end epigenetics workflow  
- Combines sequencing and machine learning  
- Strong visualization and benchmarking  

---

# Author

Amna Zulfiqar  



