# 🧬 My Bio Hub – A Collection of Bioinformatics Projects

Welcome to **My Bio Hub**, a personal repository showcasing my bioinformatics projects. This space serves as my portfolio, highlighting various computational biology workflows, data curation and analysis techniques, and bioinformatics tools.

## 🔬 What's Inside?
- **Sequence Analysis** (BLAST searches, alignments)
- **Biocuration & Data Retrieval** (NCBI, Biopython, APIs)
- **Genomics & Transcriptomics** (scRNA-seq, cancer datasets)
- **Python & SQL for Bioinformatics**

## 🚀 Current & Future Projects
✅ **Sequence Alignment and BLAST Search with Biopython** (Ongoing)  
🔜 **Protein BLAST (BLASTp) & Functional Analysis**  
🔜 **Gene Expression Data Processing & Visualization**  

This repository will be regularly updated as I explore new bioinformatics techniques and tools. Stay tuned!

---

## 📌 Projects

<details>
  <summary>🚀 **Project 1: Sequence Alignment and BLAST Search with Biopython**</summary>

### Part 1: Nucleotide BLAST (BLASTn) with NCBI
#### Overview
This part of the project demonstrates how to access and analyze nucleotide sequences using Biopython. Specifically, it retrieves sequences from a FASTA file, performs BLAST (Basic Local Alignment Search Tool) search using NCBI's `qblast` API, and processes the results to identify homologous sequences in the NCBI nucleotide database.

#### Requirements
- Python 3.x
- Biopython library
- A nucleotide sequence dataset (TP53.fna)
- Internet access (for querying NCBI)

#### Implementation
The script follows these main steps:
1. **Load the nucleotide sequences** from a FASTA file.
2. **Print sequence information** including sequence length and description.
3. **Perform BLASTn search** on each sequence using NCBI's `qblast`.
4. **Parse and display BLAST results**, including sequence IDs, descriptions, E-values, and alignments.

#### Dataset
- The dataset used is the **TP53 gene sequence**, available at:  
  [NCBI TP53 Gene](https://www.ncbi.nlm.nih.gov/gene/7157)

---

</details>

