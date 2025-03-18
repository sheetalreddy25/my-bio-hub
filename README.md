# 🧬 My Bio Hub – A Collection of Bioinformatics Projects

Welcome to **My Bio Hub**, a personal repository showcasing my bioinformatics projects. This space serves as my portfolio, highlighting various computational biology workflows, data curation and analysis techniques, and bioinformatics tools.

## 🔬 What's Inside?
- **Sequence Alignment** (BLASTn & BLASTp using NCBI)
- **Biocuration & Literature Retrieval** (PubMed, Entrez API)
- **Protein Structure & Functional Analysis** (PDB, PROSITE, SCANPROSITE)
- **Pathway & Gene Network Exploration** (KEGG Database)

## 🚀 Current & Future Projects
✅ **Sequence Alignment using NCBI BLAST** (Completed)  
🔜 **Fetch PUBMED & Nucleotide Sequences using ENTREZ**  
🔜 **Fetch Proteins from PDB**  
🔜 **PROSITE & SCANPROSITE from EXPASY**  
🔜 **Access KEGG Database**   

This repository will be regularly updated as I explore new bioinformatics techniques and tools. Stay tuned!

---

## 📌 Projects

<details>
  <summary>🚀 Project 1</summary>

# **Sequence Alignment and BLAST Search with Biopython**

### Requirements
- Python 3.x
- Biopython library
- Internet access (for querying NCBI)
- Notebooks for writing and running Python code (Jupyter, Kaggle, Google Colab, etc.)

### Implementation
The script follows these main steps:
1. **Load the nucleotide/protein sequences** from a FASTA file.
2. **Print sequence information** including sequence length and description.
3. **Perform BLASTn/BLASTp search** on each sequence using NCBI's `qblast`.
4. **Parse and display BLAST results**, including sequence IDs, descriptions, E-values, and alignments.

<details>
  <summary>🧬 Part 1</summary>

## [**Nucleotide BLAST (BLASTn) with NCBI**](https://github.com/sheetalreddy25/my-bio-hub/blob/main/nucleotide-blast-blastn-with-ncbi.ipynb)

### Overview
This part of the project demonstrates how to access and analyze nucleotide sequences using Biopython. Specifically, it retrieves sequences from a FASTA file, performs BLAST (Basic Local Alignment Search Tool) search using NCBI's `qblast` API, and processes the results to identify homologous sequences in the NCBI nucleotide database.

### Dataset
- The dataset used is the **TP53 gene sequence**, available at:  
  [NCBI TP53 Gene](https://www.ncbi.nlm.nih.gov/gene/7157)

</details>

<details>
  <summary>🧪 Part 2 (Coming Soon)</summary>

## [**Protein BLAST (BLASTp) with NCBI**](https://github.com/sheetalreddy25/my-bio-hub/blob/main/protein-blast-blastp-with-ncbi.ipynb)

### Overview
This part of the project involves performing a Protein BLAST (BLASTp) search using the translated TP53 protein sequence. BLASTp is used to compare an amino acid sequence against the NCBI protein database to identify homologous sequences.

### Dataset
- The dataset used is the **TP53 protein sequence**, available at:  
  [UniProt P04637](https://www.uniprot.org/uniprotkb/P04637/entry)
  [FASTA Download](https://rest.uniprot.org/uniprotkb/P04637.fasta)

</details>

</details>
