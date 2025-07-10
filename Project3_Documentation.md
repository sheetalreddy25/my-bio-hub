# 📘 Project 3 Documentation: Fetch Proteins from PDB

## 🧬 Overview

This project demonstrates how to **retrieve and parse 3D protein structures** using the **Protein Data Bank (PDB)** and the **Biopython PDB module**. It focuses on fetching the **TP53 tumor suppressor protein** and extracting structural metadata and chain-level details.

---

## 🛠 Requirements

- Python 3.x  
- Biopython  
- Internet access to download PDB files  
- Python notebook environment (Kaggle, Jupyter, or Google Colab)

---

## 🧬 Fetch TP53 Protein Structure

### 🎯 Objective

To **download**, **parse**, and **explore** the 3D structure of the **TP53 protein (PDB ID: 7BWN)**, including:

- General metadata (title, resolution, keywords)  
- Chain identifiers and counts  
- Residue information (IDs and amino acid codes)

### 📁 Dataset

- [RCSB Protein Data Bank](https://www.rcsb.org/structure/7BWN)

### 📓 Notebook

- *[Link to your Kaggle or GitHub Notebook]*

### 🔄 Workflow

1. Install and import **Biopython PDB modules**
2. Retrieve the PDB file for **7BWN** and save locally
3. Parse the structure using `PDBParser()`
4. Extract and display:
   - Structure title, resolution, and keywords
   - Number of models and chains
   - Chain IDs and counts of residues
5. List the first 20 residues (excluding water) with their IDs and 3-letter amino acid codes

---

## 📊 Key Takeaways

- **Biopython PDB** enables automated retrieval and parsing of structural data
- PDB metadata provides valuable experimental and biological context
- Chains and residues can be programmatically explored for custom analyses

---

## 📚 References

- [Protein Data Bank](https://www.rcsb.org/)
- [Biopython PDB Module](https://biopython.org/wiki/The_Biopython_Structural_Bioinformatics_FAQ)
- [PDB Entry: 7BWN](https://www.rcsb.org/structure/7BWN)
