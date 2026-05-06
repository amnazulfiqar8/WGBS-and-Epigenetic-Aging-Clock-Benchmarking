# WGBS and Epigenetic Aging Clock Benchmarking
# 📌 Overview

This repository combines two powerful epigenetics workflows:

🔹 WGBS DNA Methylation Analysis (Galaxy)
🔹 Epigenetic Aging Clock Benchmarking (Python + Biolearn)

Together, they provide a full-stack epigenetics pipeline from raw sequencing data → biological insights → aging prediction models.

# 🧪 Part 1: WGBS DNA Methylation Analysis (Galaxy)
# 🔬 Description

A complete Whole Genome Bisulfite Sequencing (WGBS) workflow implemented in Galaxy, based on the GTN methylation tutorial.

# 📍 Reference Genome: hg38
# 📄 Study: Lin et al., 2015

# ⚙️ Pipeline Workflow
🧰 Tools Used
Tool	Purpose
🔍 Falco	Quality Control
🧬 bwameth	Bisulfite-aware Alignment
📊 MethylDackel	Bias + Extraction
📈 computeMatrix / plotProfile	Visualization
🧪 Metilene	DMR Detection
# 📂 Dataset
Normal breast (NB)
Fibroadenoma (BT089)
Carcinomas (BT126, BT198)
Cell line (MCF7)

# 📥 Source: Zenodo (Record 557099)

# 🚀 Key Steps & Insights
1️⃣ Quality Control
High T content & low C content
✔ Expected due to bisulfite conversion
2️⃣ Alignment
Uses bwameth
✔ Handles C → T conversion
❌ Standard aligners fail
3️⃣ Methylation Bias
CpG methylation ~70–75%
Slight bias at read ends
✔ Overall stable
4️⃣ Visualization Results

# 📉 Key Finding:

Methylation drops near TSS
Suggests promoter hypomethylation

📊 Multi-sample trends:

MCF7 → highest methylation
Normal samples → lowest
Tumor samples → intermediate
5️⃣ DMR Detection
Identifies differentially methylated regions
Outputs:
Distribution plots
CpG density
Statistical significance
# 🧠 Key Concepts
Concept	Explanation
🧪 Bisulfite Conversion	C → T (unmethylated)
🧬 CpG Islands	Promoter regions
📊 DMR	Differential methylation
⚠️ Bias	Read-end artifacts
🧠 Part 2: Epigenetic Aging Clock Benchmarking
# 📊 Overview

Benchmarks 8 DNA methylation aging clocks using Biolearn across two datasets.

# 🎯 Goals:
Compare clock agreement
Measure biological age deviation
Evaluate prediction accuracy
# 📁 Datasets
Dataset	Samples	CpGs	Age Range
GSE120307	34	485K	19–54
GSE41169	95	485K	18–65

✔ Complete chronological age data available

# ⏳ Aging Clocks
Clock	Type
Horvath	First-gen
Hannum	First-gen
SkinBloodClock	First-gen
PhenoAge	Second-gen
GrimAge	Second-gen
DunedinPACE	Pace-of-aging
PCHorvath1	PCA-based
PCGrimAge	PCA-based
# ⚙️ Workflow
🔹 Install Dependencies
pip install biolearn numpy pandas matplotlib scikit-learn scipy
🔹 Run Analysis
Load datasets via DataLibrary
Load models via ModelGallery
Generate predictions
Perform visualization & evaluation
# 📊 Visualizations
🔴 Correlation Matrix
Strong agreement across most clocks
DunedinPACE shows distinct behavior
🔵 Deviation Heatmap
🔴 Older biological age
🔵 Younger biological age
Detects aging outliers
📈 Prediction Plots
Predicted vs chronological age
Ideal: diagonal alignment
📏 Metrics
Metric	Meaning
📉 MAE	Average error
📉 RMSE	Penalizes large errors
📈 Pearson r	Correlation
📊 Key Findings

✔ Horvath-based clocks perform best
✔ Strong correlation across models
✔ Dataset-dependent variability
✔ DunedinPACE captures different biology

▶️ How to Run
# Clone repo
git clone https://github.com/your-username/your-repo.git

# Navigate
cd your-repo

# Run notebook
jupyter notebook

📌 First run downloads ~500MB dataset

📦 Requirements
biolearn
numpy
pandas
matplotlib
scikit-learn
scipy
📚 References
Horvath (2013)
Hannum (2013)
Levine (2018)
Lu (2019)
Belsky (2022)
Zhang (2019)

🔗 Biolearn: https://github.com/bio-learn/biolearn

🚀 Project Highlights

✨ End-to-end epigenetics workflow
🧬 Combines sequencing + machine learning
📊 Strong visualization & benchmarking
🔬 Research-grade reproducibility

👩‍💻 Author

Amna Zulfiqar
Bioinformatics | Data Analysis | Visualization
