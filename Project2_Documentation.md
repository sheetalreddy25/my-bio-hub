# 🧬 Project 2: Fetch PUBMED & Nucleotide Sequences using ENTREZ

## 📖 Introduction
This project demonstrates how to access and retrieve biomedical literature and nucleotide sequences using **Biopython's Entrez module**. It consists of two parts:
- **Part 1**: Fetching PubMed article metadata (title, authors, journal, publication date, abstract).
- **Part 2**: Fetching nucleotide sequences (FASTA and GenBank formats) related to the TP53 gene in humans.

This project is part of a larger effort to build workflows that interact with bioinformatics databases programmatically.

---

## 🛠️ Requirements
- Python 3.x
- Biopython library
- Internet access (for querying NCBI Entrez)

---

## 🧩 Implementation

### 🧬 Part 1: Fetch PUBMED from Entrez
- Access the Entrez system and retrieve a list of available databases.
- Explore the structure and metadata of the **PubMed** database.
- Perform a search for articles related to the TP53 gene.
- Fetch and display information such as authors, title, journal name, and publication date.
- Retrieve full XML metadata for a specific PubMed ID and pretty-print it for easier readability.

> **Python notebook**:  
> [🧪 Fetch PUBMED from Entrez](https://github.com/sheetalreddy25/my-bio-hub/blob/main/fetch-pubmed-from-entrez.ipynb)

---

### 🧪 Part 2: Fetch Nucleotide Sequences from Entrez
- Search the **nucleotide** database for records related to the TP53 gene in Homo sapiens.
- Retrieve nucleotide sequence records in:
  - **FASTA format** (for raw sequence)
  - **GenBank format** (for annotated sequence features)
- Display sequences and associated metadata for the fetched records.

> **Python notebook**:  
> [🧬 Fetch Nucleotide Sequences using Entrez](https://github.com/sheetalreddy25/my-bio-hub/blob/main/fetch-nucleotide-sequences-using-entrez.ipynb)

---

## 🧬 Datasets Used
- **PubMed Database** for biomedical articles: [NCBI PubMed](https://pubmed.ncbi.nlm.nih.gov/)
- **Nucleotide Database** for genetic sequences: [NCBI Nucleotide](https://www.ncbi.nlm.nih.gov/nuccore/)
- **Gene Search Term**: `TP53[Gene] AND Homo sapiens[Organism]`

---

## 🚀 Future Scope
- Extend the Entrez workflow to automate batch downloads for multiple genes or articles.
- Perform advanced searches using MeSH terms and field-specific queries.
- Integrate the retrieved sequences into downstream analysis pipelines (e.g., sequence alignment, annotation).
