## Overview

---

This document outlines the tools and technologies I utilized during a master’s research project with Neogene Therapeutics. Specific details about the project's nature, data, and outcomes are confidential. The science underlying Neogene’s approach for T cell receptor therapy is introduced in the following page.

https://www.astrazeneca.nl/in-Nederland/Amsterdam.html

## Research Goal

---

- The research goal was to investigate if neoantigen-reactive T cell receptors (TCRs) can be predicted using gene signatures derived from RNA sequence data. To do this,
    - I evaluated the published gene sets (referenced below) for tumor-reactive T cell Receptors (CD4 and CD8 T cells) on in-house dataset.
    - I developed our own gene signatures of neoantigen-reactive TCRs to evaluate the general applicability of gene signatures.

[1] https://pubmed.ncbi.nlm.nih.gov/35113651/

## Technologies Used

---

**Programming Languages**

- **Python:** Used for single-cell RNA sequence (scRNA-seq) data process, analysis, and visualization.
- **R:** Used for scRNA-seq data process and gene set enrichment analysis.

**Libraries and Frameworks**

- Python
    - **Scanpy** : Used for analyzing single-cell RNA gene expression data.
    - **GSEAPY :** Utilized for Gene Set Enrichment Analysis
    - **CellTypist**: Employed for automated and accurate cell type classification of scRNA-seq data based on trained machine learning models.
- R
    - **Seurat :** Employed for quality control, analysis, and exploration of scRNA-seq data
    - **AUCell :** Used to identify cells with active gene sets
    - **Azimuth**: Used for reference-based mapping and prediction of cell types, enhancing annotation accuracy.
    - **projecTILs**: Utilized for analyzing tumor-infiltrating lymphocyte (TIL) profiles

**Tools and Platforms**

- **Jupyter Notebook:** Used for developing interactive code, visualizations, and presentable analyses.
- **Docker:** Employed to containerize the project environment ensuring reproducibility.

## **Skills Developed**

---

- Enhanced proficiency in single-cell RNA sequence data analysis. Specifically in
    - Data preprocessing
    - Cell clustering
    - Gene set enrichment analysis
    - Batch correction (integration)
- Acquired understanding in the bioinformatics contributions to an industrial setting.
- Deepened knowledge of T cell receptor (TCR) therapies, gaining insights into the practical applications and theoretical foundations of TCRs in immunotherapy.
- Advanced communication skills such as effectively soliciting and incorporating feedback from peers and supervisors.
- 

## **Code Samples and Resources**

---

Due to the confidentiality of the project, direct code snippets cannot be shared. However, the techniques and libraries mentioned were pivotal in achieving the project's goals. Techniques included clustering algorithms, gene set enrichment analysis, dimension reduction, and differential gene expression analysis, each tailored to the specific needs of the project. Throughout the research projects, I utilized reputable online resources, including:

- Scanpy tutorial : https://scanpy.readthedocs.io/en/stable/tutorials/index.html
- Havard Chan Bioinformatics Core Training :

https://github.com/hbctraining/scRNA-seq_online/blob/master/README.md

-
