# 📘 Project 4 Documentation: Protein Domain Analysis using ExPASy (PROSITE & ScanProsite)

## 🧬 Overview
This project focuses on identifying conserved functional domains within a protein sequence by interacting with the **ExPASy** server[cite: 1, 2]. [cite_start]It demonstrates how to retrieve expert-curated domain metadata and programmatically scan sequences for specific biochemical "signatures" or motifs that define protein families.

The project is divided into two specialized parts:
- **Part 1:** Metadata retrieval and parsing of official **PROSITE** records.
- **Part 2:** Performing live sequence scans and parsing complex XML responses via **ScanProsite**.

---

## 🧪 Part 1: PROSITE Record Retrieval from ExPASy

### 🎯 Objective
To fetch and parse the official PROSITE record (`PS00348`), which defines the conserved **p53 Family Signature**.

### 📁 Dataset
- [ExPASy PROSITE Database](https://prosite.expasy.org/)

### 📓 Notebook
- [View Python Notebook for Part 1](https://github.com/sheetalreddy25/my-bio-hub/blob/main/prosite-from-expasy.ipynb)

### 🔄 Workflow
1. **Connection**: Established a connection to the ExPASy server using `Bio.ExPASy.get_prosite_raw`.
2. **Retrieval**: Retrieved the expert-curated record for **PS00348**.
3. **Parsing**: Parsed the raw record into a Biopython `Prosite` object using `Prosite.read(handle)`.
4. **Extracted Data**: Successfully retrieved the signature pattern `M-C-N-S-S-C-[MV]-G-G-M-N-R-R` and verified its metadata, including the creation date (01-NOV-1990).

---

## 🧬 Part 2: ScanProsite Live Scan on TP53 Sequence

### 🎯 Objective
To perform a real-time scan of the human **TP53 protein sequence** to locate functional DNA-binding domains.

### 📁 Dataset
- [UniProt P04637 (TP53_HUMAN)](https://www.uniprot.org/uniprotkb/P04637/entry)

### 📓 Notebook
- [View Python Notebook for Part 2](https://github.com/sheetalreddy25/my-bio-hub/blob/main/scanprosite-from-expasy.ipynb)

### 🔄 Workflow
1. **Sequence Fetching**: Loaded the canonical human TP53 protein sequence (393 amino acids).
2. **API Submission**: Submitted the sequence to the **ScanProsite API** using `ScanProsite.scan()`.
3. **Advanced Parsing**: Implemented `xml.etree.ElementTree` to handle raw XML data directly.
4. **Namespace Management**: Defined the `urn:expasy:scanprosite` namespace to navigate the response tree.
5. **Data Extraction**: Identified the signature ID (`PS00348`), start position (`237`), and stop position (`249`).

---

## ⚠️ Technical Note: Biopython and ScanProsite API Incompatibility

A critical component of this project was overcoming a modern technical limitation: the **incompatibility between current Biopython high-level functions and the ScanProsite API**.

* **Format Mismatch**: While Biopython’s `Prosite.read()` successfully parses static record files (as seen in Part 1), the high-level `ScanProsite.read()` function often fails with live API results.
* **The Problem**: The modern ExPASy server returns results in a complex **XML format** utilizing a specific namespace (`urn:expasy:scanprosite`). Legacy Biopython parsers often fail to account for this namespace, leading to empty results.
* **The Solution**: By reading the raw "handle" as a string and using `xml.etree.ElementTree`, we manually mapped the data. This allows for direct navigation of `sp:match` tags, ensuring the tool remains functional even if server record formats change.

---

## 📚 References
* [ExPASy PROSITE & ScanProsite](https://prosite.expasy.org/)
* [Biopython Documentation](https://biopython.org/wiki/Documentation)
* [UniProt Database](https://www.uniprot.org/)
