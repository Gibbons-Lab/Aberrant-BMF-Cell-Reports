[Link to Cell Reports Medicine article](https://www.cell.com/cell-reports-medicine/fulltext/S2666-3791(24)00360-4?_returnURL=https%3A%2F%2Flinkinghub.elsevier.com%2Fretrieve%2Fpii%2FS2666379124003604%3Fshowall%3Dtrue)

# INSTRUCTIONS

# base_final.ipynb

## Purpose:
### This Jupyter Notebook performs the initial steps in the analysis of aberrant bowel movement frequencies (BMF) and their correlation with gut microbiome and organ function. It includes the following tasks:
### 1.  Data Import and Preprocessing: 
Imports raw data from Arivale snapshots and performs necessary cleaning, filtering, and transformation steps.
### 2.  BMF Cohort Identification: 
Defines criteria for BMF and identifies cohorts of individuals based on their bowel movement patterns.
### 3.  Data Export: 
Saves BMF cohort data into separate CSV files (e.g., `asvs.csv`) for subsequent analyses.
### 4.  Descriptive Statistics:
Calculates and reports basic descriptive statistics for each BMF cohort, such as mean age, gender distribution, and other relevant metrics.

## Input:
### - `arivale_snapshot`: 
Raw data from Arivale snapshots, containing relevant health and lifestyle information for each individual.

## Output:
### - `[multi-omic].csv`: 
CSV files containing data for each identified BMF cohort.

## Parameters:
### - `gender,age,BMI_CALC,vendor_dashboard,eGFR,CRP,A1C,LDL,PC[1-3],taxa_[taxonomic_classification],[metabolite_IDs],[clinical_chemistries],etc.`: 
List of parameters spanning the multi-omic data analyses needs and their BMF subcohorts (e.g., metabolomics).

## Usage & Dependencies:
### 1.  Set up environment & dependencies:
- Python 
- pandas
- numpy
- seaborn

Ensure that the required Python packages (pandas, numpy, etc.) and dependencies are installed and loaded from the first few cells.
### 2. Specify input file:
Load the `arivale_snapshot` path within the notebook.
### 3. Run the notebook: 
Execute the notebook cells sequentially or in desired chunks to complete the data import, preprocessing, cohort identification, and descriptive statistics calculation.
### 4.  Review outputs: 
Examine the generated CSV files and descriptive statistics summary.

# metabolomics_eGFRanalysis_final.ipynb

## Purpose:
This Jupyter Notebook investigates the relationship between BMF-associated metabolites and kidney function (estimated glomerular filtration rate - eGFR). It utilizes data from Arivale snapshots and the results of LIMMA regressions to perform an OLS regression analysis, outputting statistical summaries and plots.**
## Input:
### - Arivale snapshot data with relevant metabolomics and eGFR information.
### - BMF-associated metabolites identified through LIMMA regressions.
## Output:
### - Statistical summaries of the OLS regression analysis (e.g., coefficients, p-values).
### - Plots visualizing the relationships between metabolites and eGFR.
## Usage & Dependencies:
### - See base_final.ipynb for similar instructions and dependencies. Run the notebook to execute the analysis and generate the output files.

# R Analysis Scripts (CORNCOB, LIMMA, POLR, etc.) and workspaces

## Purpose:
This collection of R scripts performs statistical analyses on the preprocessed data generated by the Jupyter Notebooks. They leverage various R packages (e.g., bioconductor, tidyverse) to conduct regressions, including CORNCOB, LIMMA, and POLR. The scripts output graphical visualizations and summary statistics to aid in interpretation of the results.

## Input:
### - CSV files generated by the Jupyter Notebooks (e.g., BMF cohort data, metabolomics data, eGFR data).

## Output:
### - Graphical representations of the analysis results (e.g., plots, heatmaps).
### - Summary statistics tables (e.g., regression coefficients, p-values).

## Usage & Dependencies:
### 1. Set up environment & dependencies:
- R
- bioconductor
- tidyverse
- CORNCOB
- LIMMA
- polr

Ensure that the required R packages are installed and loaded.
### 2. Specify input files:
Adjust file paths in the scripts to match your directory structure.
### 3. Run the scripts:
Execute the scripts in R or RStudio to perform the analyses and generate the outputs.



