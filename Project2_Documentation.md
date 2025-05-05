# 📘 Project 2 Documentation: Fetch PUBMED & Nucleotide Sequences using ENTREZ

## 🧬 Overview

This project demonstrates how to access and retrieve biomedical literature and nucleotide sequences using the **Entrez system** from **NCBI**, powered by **Biopython**. It is divided into two parts:

- Part 1: Fetching PubMed article metadata using **Entrez**
- Part 2: Fetching nucleotide sequences (FASTA and GenBank) using **Entrez**

---

## 🛠 Requirements

- Python 3.x  
- Biopython  
- Internet access for querying NCBI Entrez  
- Python notebook environment (Kaggle, Jupyter, or Google Colab)

---

## 🧬 Part 1: Fetch PUBMED using Entrez

### 🎯 Objective

To retrieve and display metadata from **PubMed** articles related to the **TP53 gene**.

### 📓 Notebook

- [View Python Notebook for Part 1](https://github.com/sheetalreddy25/my-bio-hub/blob/main/fetch-pubmed-from-entrez.ipynb)

### 🔄 Workflow

1. Access Entrez and list available databases  
2. Explore the PubMed database metadata  
3. Search for articles related to "TP53", and display the top 20 hits  
4. Display article metadata (authors, title, journal, date) for a couple of PubMed IDs
5. Fetch and pretty-print raw XML for a specific PubMed ID

---

## 🧪 Part 2: Fetch Nucleotide Sequences using Entrez

### 🎯 Objective

To retrieve **nucleotide sequences** related to the **TP53 gene** in **Homo sapiens** from the NCBI **nucleotide** database.

### 📓 Notebook

- [View Python Notebook for Part 2](https://github.com/sheetalreddy25/my-bio-hub/blob/main/fetch-nucleotide-sequences-using-entrez.ipynb)

### 🔄 Workflow

1. Search the nucleotide database for TP53 in humans  
2. Fetch and display top 20 result IDs  
3. Retrieve a nucleotide sequence in **FASTA** format  
4. Retrieve the same sequence in **GenBank** format  
5. Display detailed sequence metadata

---

## 📊 Key Takeaways

- Entrez allows programmatic access to NCBI databases  
- PubMed and Nucleotide records can be queried and parsed easily  
- Biopython streamlines querying, parsing, and formatting NCBI data  

---

## 📚 References

- [NCBI Entrez](https://www.ncbi.nlm.nih.gov/books/NBK25497/)  
- [Biopython Documentation](https://biopython.org/wiki/Documentation)  
- [PubMed](https://pubmed.ncbi.nlm.nih.gov/)  
- [Nucleotide Database](https://www.ncbi.nlm.nih.gov/nuccore/)
