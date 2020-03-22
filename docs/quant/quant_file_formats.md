To represent quantification and extract meaningful insight there are two file formats that we define:

 1. Minimal Feature Input Format (MFIF) - This describes feature quantification
 1. Annotation Format  - This describes the experimental design and conditions to meaningfully compare

These two files are used for creating a reanalysis for MassIVE.quant as well as enabling you to compute statistics with the MSstats workflow. 

 ## MFIF Documentation

This describes the quantification format that will be required. The format must be tab separated.

[Example File](example_files/50proteins_iprg_yaff.txt)

| Header | Description | Required |
|--------|-------------|----------|
| Protein | Name of the protein | Proteomics |
| Unmodified Peptide | Sequence of peptide without modifications | Proteomics |
| Modified Peptide | Sequence of peptide including modifications | Proteomics |
| Structure | Name of the structure | Metabolomics |
| Feature Name | Feature name for structure | Metabolomics |
| m/z | Quantification Value | All | 
| Charge | Precursor charge | All | 
| Run | Sample/Run Name | All | 
| Intensity | Quantification Value | All | 


## Annotation Format

[Example File](ftp://massive.ucsd.edu/RMSV000000306/2020-03-21_nuno_750cbdff/metadata/MSV000080026_mplex_calu3_H1N1_response.csv)

| Header | Description | Required |
|--------|-------------|----------|
| Run  | File name for sample  | Yes |
| Cohort | High Level Grouping | Yes |
| Condition | Comparison Condition | Yes |
| BioReplicate | Biological Replicate | Yes |
| Experiment | Can be anything | Yes |
| Dataset |  MassIVE Dataset Accession  | No (Only for Reanalysis Attachement) |

