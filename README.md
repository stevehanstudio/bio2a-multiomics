# **BIO2A Bioinformatics Group Project - Spring 2025**

## **Project Overview**
This project is part of the **BIO2A Bioinformatics class at Las Positas College (Spring 2025)**. The goal is to analyze **multi-omics data** using **single-cell RNA sequencing (scRNA-seq)** and **single-cell ATAC sequencing (scATAC-seq)** datasets.

## **Team Members**
- **Steve Han**
- **Jett Spitzer**
- **Farahnaz Moazezi**

## **Project Setup**

### **Prerequisites**
Ensure you have the following installed before proceeding:
- **Python 3.x**
- **Jupyter Notebook**
- **Visual Studio Code (VS Code)**

### **Installation**
#### **1. Clone the Repository**
```bash
git clone git@github.com:stevehanstudio/bio2a-multiomics.git
cd bio2a-multiomics
```

#### **2. Create a Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

#### **3. Install Required Packages**
```bash
pip install -r requirements.txt
```

## **Project Structure**
```
bio2a-multiomics/
│
├── data/
│   └── GSE126074/
│       ├── GSE126074_AdBrainCortex_SNAREseq_cDNA.counts.mtx.gz
│       ├── GSE126074_AdBrainCortex_SNAREseq_cDNA.barcodes.tsv.gz
│       ├── GSE126074_AdBrainCortex_SNAREseq_cDNA.genes.tsv.gz
│       ├── GSE126074_AdBrainCortex_SNAREseq_chromatin.counts.mtx.gz
│       ├── GSE126074_AdBrainCortex_SNAREseq_chromatin.barcodes.tsv.gz
│       └── GSE126074_AdBrainCortex_SNAREseq_chromatin.peaks.tsv.gz
│
├── analyze_gse126074.ipynb
├── requirements.txt
├── README.md
└── .gitignore
```

## **Dataset**
The dataset used in this project is obtained from the [NCBI Gene Expression Omnibus (GEO) GSE126074](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi) and located in the **`data/GSE126074`** folder. It contains **single-cell RNA-seq** and **single-cell ATAC-seq** data from the **GSE126074 study**.

### **Dataset Description**
#### **scRNA-seq Data**
- `GSE126074_AdBrainCortex_SNAREseq_cDNA.counts.mtx.gz` – **Gene expression counts matrix**
- `GSE126074_AdBrainCortex_SNAREseq_cDNA.barcodes.tsv.gz` – **Barcodes for scRNA-seq data**
- `GSE126074_AdBrainCortex_SNAREseq_cDNA.genes.tsv.gz` – **Gene annotations**

#### **scATAC-seq Data**
- `GSE126074_AdBrainCortex_SNAREseq_chromatin.counts.mtx.gz` – **Peak accessibility counts matrix**
- `GSE126074_AdBrainCortex_SNAREseq_chromatin.barcodes.tsv.gz` – **Barcodes for scATAC-seq data**
- `GSE126074_AdBrainCortex_SNAREseq_chromatin.peaks.tsv.gz` – **Peak annotations**

## **Analysis Overview**
The **Jupyter Notebook (`analyze_gse126074.ipynb`)** includes the following steps:
1. **Loading** the scRNA-seq and scATAC-seq datasets
2. **Preprocessing** the data for analysis
3. **Visualizing** gene expression and peak accessibility distributions
4. **Performing multi-omics analysis** using the **MuData framework**
5. **Applying UMAP and clustering** to explore results

## **License**
This project is licensed under the **MIT License**.

## **Acknowledgments**
Special thanks to our professor **Dr. Kai Blaisdell** for guidance and support.

## **References**

The paper by Xiao et al. (2024) discusses and benchmarks 12 different multi-omics integration algorithms for single-cell RNA-seq (scRNA-seq) and single-cell ATAC-seq (scATAC-seq) data. In this project, we utilized the multi-omics GSE126074 dataset referenced in their study.  The dataset was originally generated and published in paper by Chen et al (2019).

Xiao, C., Chen, Y., Meng, Q., Wei, L., & Zhang, X. (2024). Benchmarking multi-omics integration algorithms across single-cell RNA and ATAC data. Briefings in Bioinformatics, 25(2), bbae095. [https://doi.org/10.1093/bib/bbae095](https://doi.org/10.1093/bib/bbae095)

Chen S, Lake BB, Zhang K. (2019) High-throughput sequencing of the transcriptome and chromatin accessibility in the same cell. *Nature Biotechnolology*, 37,1452–1457. [https://doi.org/10.1038/s41587-019-0290-0](https://doi.org/10.1038/s41587-019-0290-0)


