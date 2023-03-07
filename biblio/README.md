# Folder containing bibliography files

The files must be in the bibtex format.

## How to create corresponding md files?

Nelle created a Python script to parse and generate automatically md files from a bibtex bibliography file. 
To run it:

```bash
# Activate a dedicated virtual environment?
conda create --name webenv
conda activate webenv

# First install the required library bibtextparser:
conda install -c conda-forge bibtexparser

# Create an output directory to store the generated md:
mkdir results_03_2023

# Then run the script:
python ../scripts/convert_bibtex_to_md.py 2023-03_MyPapers.bib results_03_2023/
```
