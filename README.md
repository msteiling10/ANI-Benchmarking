# ANI-Benchmarking

## Introduction
This code is being developed to benchmark three genome comparison tools against one another. The selected tools are currently FastANI, PyANI, and MASH. FastANI and PyANI produce percent identities, while MASH produces a value between 0-1. MASH results can be converted into a comparable percentage with simple math. 

## Clone This Repository

First, check that git is installed in your environment
```Bash
git --version
```
Next, navigate to the directory you plan to work in
```Bash
cd /path/to/directory/or/folder
```
Finally, clone this repository in your working directory
```Bash
git clone git@github.com:msteiling10/ANI-Benchmarking.git
```

## Begin Install of Necessary Tools
To install necessary tools, the conda_maker.yml can be uploaded to the working directory. Then the text file, conda_maker_code.txt can be opened and the text copied and pasted into the terminal to install all tools. Additionally, you might need to install python pandas and python biopython. This can be done with the following code run in the terminal:

```bash
pip install pandas
pip install biopython
```

You can check versions via these examples pasted in the terminal:

```bash
fastani --version
mash --version
pyani --version 
```

Ensure the conda envrionment is activated, this code is available in the <ins>conda_maker_code.txt</ins> and can be copied and pasted into the terminal. This should allow necessary tools to be downloaded in an easy and streamlined manner. 

## Basics to Run Code:

A TSV must be downloaded from the NCBI Genome Website -- https://www.ncbi.nlm.nih.gov/datasets/genome/
Start by searching for the organism needed
Ensure the following headers are included in the tsv:
Assembly
BioSample
GenBank
Level
RefSeq
Release date
Sequencing technology
Submitter
Annotation
CheckM completeness (%)
CheckM contamination (%)
Scaffolds
Size (Mb)

Upload the TSV to the working directory.
In CONFIGURATION ZONE of the ANI Pipeline add the path of the tsv and the name of the organism for outfiles. 

Running the code can be done with the following command:
python ANI_Pipeline_V2.py
