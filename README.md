# my-bio-hub

# Sequence Alignment and BLAST Search with Biopython

This project demonstrates how to access and analyze nucleotide and protein sequences using Biopython. 
It focuses on performing BLAST (Basic Local Alignment Search Tool) queries through NCBI's `qblast` API 
to find homologous sequences in bioinformatics databases.

## Project Structure
- **Part 1: Nucleotide BLAST (BLASTn) with NCBI**
  - Reads nucleotide sequences from a FASTA file.
  - Performs BLASTn search against the NCBI nucleotide database.
  - Parses and displays BLAST results, including sequence IDs, descriptions, E-values, and alignments.

- **Part 2: Protein BLAST (BLASTp) with NCBI** *(Coming Soon)*
  - Translates nucleotide sequences into proteins.
  - Performs BLASTp search for homologous protein sequences.

## Dataset
- The dataset used is the **TP53 gene sequence**, available at:  
  [NCBI TP53 Gene](https://www.ncbi.nlm.nih.gov/gene/7157)

## Requirements
- Python 3.x
- Biopython (`pip install biopython`)
- Internet access for querying NCBI

## Usage
Run the following command in a Jupyter Notebook or Python script:
```python
!pip install biopython
from Bio.Blast import NCBIWWW 
from Bio import SeqIO, SearchIO 
