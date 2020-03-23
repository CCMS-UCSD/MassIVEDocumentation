To represent quantification and extract meaningful insight there are two file formats that we define:

 1. Minimal Feature Input Format (MFIF) - This describes feature quantification
 1. Annotation Format - This describes the experimental design and conditions to meaningfully compare

These two files are used for creating a reanalysis for MassIVE.quant as well as enabling you to compute statistics with the MSstats workflow. 

 ## MFIF Documentation

This describes the quantification format that will be required. The format must be tab separated.

[Example File](example_files/50proteins_iprg_mfif.txt)

| Header | Description | Required |
|--------|-------------|----------|
| Protein | Name of the protein | Proteomics |
| Unmodified Peptide | Sequence of peptide without modifications | Proteomics |
| Modified Peptide | Sequence of peptide including modifications | Proteomics |
| Compound | Name of the compound | Metabolomics |
| Feature ID | Feature ID | Metabolomics |
| m/z | Mass to charge ratio | All | 
| Charge | Precursor charge | All | 
| Run | Sample/Run Name | All | 
| Intensity | Intensity for the feature | All | 


## Annotation Format

[Example File](ftp://massive.ucsd.edu/RMSV000000306/2020-03-21_nuno_750cbdff/metadata/MSV000080026_mplex_calu3_H1N1_response.csv)

| Header | Description | Required |
|--------|-------------|----------|
| Run  | File name for sample  | Yes |
| Subject | An individual from whom multiple samples maybe aquired for the purpose of the study. | No |
| Cohort | A set of subjects aggregated for the purpose of the study | Yes* |
| Condition | Original dataset study variable | Yes* |
| TimePoint | Different time points within the same experiment | Yes* |
| BioReplicate | Biological replicate | Yes |
| Experiment | Technical replicate | Yes |
| Fraction | Fraction number | No |
| Disease | Disease name | Yes* |
| Tissue | Tissue name | Yes* |
| Species | Species name | Yes* |
| Enzyme | Enzyme name | No |
| Notes | Other notes | Yes |
| Dataset |  MassIVE Dataset Accession  | No (Only for Reanalysis Attachement) |

 \*One of the following must be in the file.
