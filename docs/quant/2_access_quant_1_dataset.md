

Each dataset has its own page. Here is the example of one dataset, MSV000079843.

### Dataset page
If you know the dataset MSV ID or PXD ID, such as MSV000079843 or PXD015300, you can search in the main MassIVE webpage. 

**_todo : 1) new capture for whole page_**
![](img/access_quant_reanalyses/datasetpage_show_container_iprg.png)


### Title

It shows the title that submitter provided in `MassIVE dataset Submission` workflow. For this dataset, 'iPRG2015'.


### Description

It shows the description that submitter wrote in `MassIVE dataset Submission` workflow.


### Contact

It shows the contact information about the owner or submitter of this dataset.


### Publications

It shows the publication related to this dataset. The publication includes all the details related to this dataset.


### Dataset Reanalyses

At the bottom of this page, there is the table to show the list of reanalyses in this dataset. For this example, there are 3 containers and 51 reanalyses available in this dataset. Each container and reanalysis has their own RMSV ID. If you click any RMSV ID, you will move to the webpage for specific RMSV. 


### Summary table for one reanalysis

There is the summary box on the left of this page. It shows the simple summary about experimental design and quantification/statistical analysis for this reanalysis.

**_todo : 2) new capture for summary table_**

- **Owner** column : 'Owner' means the submitter who designed the experiments, set up this dataset, and submitted files, including raw.files, for the first time. The column of 'Owner' shows the summary of what the owner submitted.

- **Reanalysis** column : First, it shows how many reanalyses are included in this dataset. The column of 'Reanalyses' is the summary of all reanalyses in this dataset.

- **N/A** : Not available. For example, MassIVE.quant can't count the number of Conditions, Biological Replicates, or Technical Replicates if the owner didn't submit any files in `Metadata` category. Then, 'N/A' will be shown. 



1. **Experimental Design**: The summary of detected experimental design from `Metadata` category.

    - **Condition**: Number of distinct conditions across all analyses (original submission and reanalyses) associated with this dataset. Distinct condition labels are counted across all files submitted in the `Metadata` category having a `Condition` column in this dataset. 
    For this container, there are four conditions across all files in the `Metadata` category in this container's reanalyses.

    - **Biological Replicates**: Number of distinct biological replicates across all analyses (original submission and reanalyses) associated with this dataset. Distinct replicate labels are counted across all files submitted in the `Metadata` category having a `BioReplicate` or `Replicate` column in this dataset.
    For this container, four unique IDs for biological replicates are available across all 'annotation.csv' files in the `Metadata` category in this container's reanalyses.

    - **Technical Replicates**: Number of distinct technical replicates across all analyses (original submission and reanalyses) associated with this dataset. The technical replicate count is defined as the maximum number of times any one distinct combination of condition and biological replicate was analyzed across all files submitted in the `Metadata` category. In the case of fractionated experiments, only the first fraction is considered.
    For this container, maximum three technical replicates for the corresponding biological replicate are available across all reanalyses in this container.

2. **Identification Result**: The summary of the result for identification searching from `xx` category.

    - **Protein (Human, Remapped)**: Originally identified proteins that were automatically remapped by MassIVE to proteins in the SwissProt human reference database.
    
    - **Proteins (Reported)**: Number of distinct protein accessions reported by originally submitted search results.
    
    - **Peptides**: 
    
    - **Variant Peptides**:
    
    - **PSMs**: 
    
3. **Quantification Result**: The summary of the result for statistical analysis from `Statistical Analysis of Quantified Analytes` category.

    - **Differential proteins**: Number of distinct proteins found to be differentially abundant in at least one comparison across all analyses (original submission and reanalyses) associated with this dataset. A protein is differentially abundant if its change in abundance across conditions is found to be statistically significant with an adjusted p-value <= 0.05 and lists no issues associated with statistical tests for differential abundance. Distinct protein accessions are counted across all files submitted in the `Statistical Analysis of Quantified Analytes` category having a `Protein` column in this dataset. 
    For this container, there are xx reanalyses including the table for the result of statistical analysis in the `Statistical Analysis of Quantified Analytes` category. Ten proteins are significantly different for at least one pairwise comparisons across xx reanalyses.

    - **Quantified proteins**: Number of distinct proteins quantified across all analyses (original submission and reanalyses) associated with this dataset. Distinct protein accessions are counted across all files submitted in the `Statistical Analysis of Quantified Analytes` category having a `Protein` column in this dataset.
    For this container, 2,875 proteins were quantified and tested by MSstats across xx reanalyses in this container.
    


### [Button : FTP Download](2_download_files.md)

All the submitted files in the reanalysis are available for downloading from FTP. See [here](2_download_files.md) for detailed instructions on how to download the files in any category.


