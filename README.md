### PaRSnIP
PaRSnIP is a sequence-based protein solubility predictor.

## Motivation
Protein solubility can be a decisive factor in both research and production efficiency, and in silico sequence-based predictors, which can accurately estimate solubility outcomes, are highly sought of.

## Installation

# Requirements 
- R (https://www.r-project.org)
  - R libraries
    - bio3d
    - stringr
    - Interpol
    - zoo
    - h2o (version 3.10.0.8) (https://cran.r-project.org/web/packages/h2o/index.html) (see "Old sources")
- SCRATCH (version SCRATCH-1D release 1.1) (http://scratch.proteomics.ics.uci.edu, Downloads: http://download.igb.uci.edu/#sspro)


# Run 
PaRSnIP can be run in the command line

Three input arguments are necessary to run the software.
  1. Protein sequence of interest in fasta format (https://en.wikipedia.org/wiki/FASTA_format)
  2. SCRATCH run path (usually it is in the directory where you installed SCRATCH adding the following SCRATCH-1D_1.1/bin/run_SCRATCH-1D_predictors.sh)
  3. The PaRSnIP h2o model (PaRSnIP_training_model)

# Execute in the command line
R --vanilla < PaRSnIP.R argument1 argument2 argument3

(Example: R --vanilla < /home/user/software/PaRSnIP.R test_protein.fa /home/user/software/SCRATCH/SCRATCH-1D_1.1/bin/run_SCRATCH-1D_predictors.sh /home/user/software/PaRSnIP_training_model)

# Result
Probability that the protein test sequence is soluble will be saved in file result.txt

## Tests

R --vanilla < PaRSnIP.R P21.fasta ..../SCRATCH-1D_1.1/bin/run_SCRATCH-1D_predictors.sh PaRSnIP_training_model output.txt

# Reference
Reda Rawi, Raghvendra Mall, Khalid Kunji, Chen-Hsiang Shen, Peter D Kwong, Gwo-Yu Chuang; PaRSnIP: sequence-based protein solubility prediction using gradient boosting machine, Bioinformatics, Volume 34, Issue 7, 1 April 2018, Pages 1092–1098, https://doi.org/10.1093/bioinformatics/btx662

# Contact
Reda Rawi: reda.rawi@nih.gov
