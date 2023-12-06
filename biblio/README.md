# Folder containing bibliography files

The files must be in the bibtex format.

## Updating the bibliography, as of Dec 2023

The updated biblio was exported from the Zotero collection "My papers" as a bibtex file: `2023-12_My_papers.bib`


```bash
# First install the required library bibtextparser:
conda activate webenv

# Create an output directory to store the generated md:
mkdir results_12_2023

# Then run the script:
python ../scripts/convert_bibtex_to_md.py 2023-12_My_papers.bib results_12_2023/

# Then copy the publications in the right folder, to add publications to the website:
cp results_12_2023/*.md ../_publications/

conda deactivate
```

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

# Then copy the publications in the right folder, to add publications to the website:
cp results_03_2023/*.md ../_publications/
```