# 📘 Project 4 Documentation: Protein Domain Analysis using ExPASy (PROSITE & ScanProsite)

## 🧬 Overview
[cite_start]This project focuses on identifying conserved functional domains within a protein sequence by interacting with the **ExPASy** server[cite: 1, 2]. [cite_start]It demonstrates how to retrieve expert-curated domain metadata and programmatically scan sequences for specific biochemical "signatures" or motifs that define protein families[cite: 2, 3].

The project is divided into two specialized parts:
- [cite_start]**Part 1:** Metadata retrieval and parsing of official **PROSITE** records[cite: 3].
- [cite_start]**Part 2:** Performing live sequence scans and parsing complex XML responses via **ScanProsite**[cite: 2].

---

## 🧪 Part 1: PROSITE Record Retrieval from ExPASy

### 🎯 Objective
[cite_start]To fetch and parse the official PROSITE record (`PS00348`), which defines the conserved **p53 Family Signature**[cite: 3].

### 📁 Dataset
- [cite_start][ExPASy PROSITE Database](https://prosite.expasy.org/) [cite: 3]

### 📓 Notebook
- [cite_start][View Python Notebook for Part 1](https://github.com/sheetalreddy25/my-bio-hub/blob/main/prosite-from-expasy.ipynb) [cite: 3]

### 🔄 Workflow
1. [cite_start]**Connection**: Established a connection to the ExPASy server using `Bio.ExPASy.get_prosite_raw`[cite: 3].
2. [cite_start]**Retrieval**: Retrieved the expert-curated record for **PS00348**[cite: 3].
3. [cite_start]**Parsing**: Parsed the raw record into a Biopython `Prosite` object using `Prosite.read(handle)`[cite: 3].
4. [cite_start]**Extracted Data**: Successfully retrieved the signature pattern `M-C-N-S-S-C-[MV]-G-G-M-N-R-R` and verified its metadata, including the creation date (01-NOV-1990)[cite: 3].

---

## 🧬 Part 2: ScanProsite Live Scan on TP53 Sequence

### 🎯 Objective
[cite_start]To perform a real-time scan of the human **TP53 protein sequence** to locate functional DNA-binding domains[cite: 2].

### 📁 Dataset
- [cite_start][UniProt P04637 (TP53_HUMAN)](https://www.uniprot.org/uniprotkb/P04637/entry) [cite: 2]

### 📓 Notebook
- [cite_start][View Python Notebook for Part 2](https://github.com/sheetalreddy25/my-bio-hub/blob/main/scanprosite-from-expasy.ipynb) [cite: 2]

### 🔄 Workflow
1. [cite_start]**Sequence Fetching**: Loaded the canonical human TP53 protein sequence (393 amino acids)[cite: 2].
2. [cite_start]**API Submission**: Submitted the sequence to the **ScanProsite API** using `ScanProsite.scan()`[cite: 2].
3. [cite_start]**Advanced Parsing**: Implemented `xml.etree.ElementTree` to handle raw XML data directly[cite: 2].
4. [cite_start]**Namespace Management**: Defined the `urn:expasy:scanprosite` namespace to navigate the response tree[cite: 2].
5. [cite_start]**Data Extraction**: Identified the signature ID (`PS00348`), start position (`237`), and stop position (`249`)[cite: 2].

---

## ⚠️ Technical Note: Biopython and ScanProsite API Incompatibility

A critical component of this project was overcoming a modern technical limitation: the **incompatibility between current Biopython high-level functions and the ScanProsite API**.

* [cite_start]**Format Mismatch**: While Biopython’s `Prosite.read()` successfully parses static record files (as seen in Part 1), the high-level `ScanProsite.read()` function often fails with live API results[cite: 2, 3].
* [cite_start]**The Problem**: The modern ExPASy server returns results in a complex **XML format** utilizing a specific namespace (`urn:expasy:scanprosite`)[cite: 2]. [cite_start]Legacy Biopython parsers often fail to account for this namespace, leading to empty results[cite: 2].
* [cite_start]**The Solution**: By reading the raw "handle" as a string and using `xml.etree.ElementTree`, we manually mapped the data[cite: 2]. [cite_start]This allows for direct navigation of `sp:match` tags, ensuring the tool remains functional even if server record formats change[cite: 2].

---

## 📚 References
* [cite_start][ExPASy PROSITE & ScanProsite](https://prosite.expasy.org/) [cite: 2, 3]
* [cite_start][Biopython Documentation](https://biopython.org/wiki/Documentation) [cite: 2, 3]
* [cite_start][UniProt Database](https://www.uniprot.org/) [cite: 2]
