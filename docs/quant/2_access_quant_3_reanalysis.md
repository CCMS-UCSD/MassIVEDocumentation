
Each individual reanalysis has its own page. Here is the example of one reanalysis, RMSV000000248.29.

### Reanalysis page
If you know the reanalysis ID, such as RMSV0000248.29, you can search in the main MassIVE webpage. Also you can access from either the dataset or the container, for example, MSV000079843 or RMSV000000249, for this reanalysis.

**_todo : 1) new capture for whole page_**
![](img/access_quant_reanalyses/datasetpage_show_reanalysis_iprg.png)

The title and description for this reanalysis are available here.

### Summary table for one reanalysis

There is the summary box on the left of this page. It shows the simple summary about experimental design and quantification/statistical analysis for this reanalysis.

**_todo : 2) new capture for summary table_**

1. **Experimental Design**: The summary of detected experimental design from `Metadata` category.

    - **Condition**: Number of distinct conditions analyzed in this reanalysis. Distinct condition labels are counted across all files submitted in the `Metadata` category having a "Condition" column in this reanalysis. For this reanalysis, there are four conditions from 'annotation.csv' file in the `Metadata` category.

    - **Biological Replicates**: Number of distinct biological replicates in this reanalysis. Distinct replicate labels are counted across all files submitted in the `Metadata` category having a `BioReplicate` or `Replicate` column in this reanalysis. For this reanalysis, there is `BioReplicate` column in 'annotation.csv' file. Four unique ID for biological replicates are available.

    - **Technical Replicates**: Number of distinct technical replicates in this reanalysis. The technical replicate count is defined as the maximum number of times any one distinct combination of condition and biological replicate was analyzed in files submitted in the `Metadata` category. In the case of fractionated experiments, only the first fraction is considered. For this reanalysis, there is one file, called 'annotation.csv' in the `Metadata` category. Each biological replicate is assigned in one condition. There are three unique 'Run' for each biological replicate, which are the technical replicates for the corresponding biological replicate.


2. **Quantification Result**: The summary of the result for statistical analysis from `Statistical Analysis of Quantified Analytes` category

    - **Differential proteins**: Number of distinct proteins found to be differentially abundant in at least one comparison in this reanalysis. A protein is differentially abundant if its change in abundance across conditions is found to be statistically significant with an adjusted p-value <= 0.05 and lists no issues associated with statistical tests for differential abundance. Distinct protein accessions are counted across all files submitted in the `Statistical Analysis of Quantified Analytes` category having a `Protein` column in this reanalysis. For this reanalysis, there is one table for the result of statistical analysis in the `Statistical Analysis of Quantified Analytes` category (_Choi2017_DDA_MaxQuant_testResult_byMSstats.csv_). In this table, ten proteins are signigicantly different for at least one pairwise comparions. There are 'adj.pvalue' column and 'issue' column. The proteins ('Protein' column) and comparisons ('Label' column) with 'adj.pvalue' <= 0.05 and 'issue' = NA are detected as statistically significant.

    - **Quantified proteins**: Number of distinct proteins quantified in this reanalysis. Distinct protein accessions are counted across all files submitted in the `Statistical Analysis of Quantified Analytes` category having a `Protein` column in this reanalysis. For this reanalysis, 2,875 proteins were quantified and tested by MSstats. The table for the result of statistical analysis in the `Statistical Analysis of Quantified Analytes` category (_Choi2017_DDA_MaxQuant_testResult_byMSstats.csv_) includes the result for 2.875 proteins.
    

### [Button : FTP Download](2_download_files.md)

All the submitted files in the reanalysis are available for downloading from FTP. See [here](2_download_files.md) for detailed instructions on how to download the files in any category.


### [Button : Browse Quantification Results](2_browse_files.md)

You can browse the quantification results for the reanalysis by clicking on **Browse Quantification Results** from the reanalysis page. See [here](2_browse_files.md) for detailed instructions on how to browse the files in the `Quantification Result` or `Statistical Analysis of Quantified Analytes` categories.


### [Button : Browse Metadata](2_browse_files.md)

You can browse the metadata for the reanalysis by clicking on **Browse Metadata** from the reanalysis page. See [here](2_browse_files.md) for detailed instructions on how to browse the files in the `Metadata` category.
