
To represent quantification and extract meaningful insight there are two file formats that we define:

1. Minimal Feature Input Format (MFIF) - This describes feature quantification
1. Annotation Format  - This describes the experimental design and conditions to meaningfully compare

These two files are used for creating a reanalysis for MassIVE.quant as well as enabling you to compute statistics with the MSStats workflow. 

## MFIF Documentation

This describes the quantification format that will be required. 

[Example File](example_files/Choi2017_DDA_Skyline_input_50_minimal.csv)

| Header | Description | Required |
|--------|-------------|----------|
| Protein Name | Name of the Protein | Yes |
| PeptideSequence | Sequence of Peptide | Yes |
| PeptideModifiedSequence | PeptideModifiedSequence | Yes |
| Precursor Charge | Charge | Yes | 
| Fragmentation | Always list precursor | Yes | 
| FileName | Sample Name | Yes | 
| Area | Quantification Value | Yes | 


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

