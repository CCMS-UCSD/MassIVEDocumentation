
Each container, including at least one reanalysis, has its own page. Here is the example of one contaion, RMSV000000248. It includes reanalysis (RMSV000000248.29).

If there are multiple experiments in one MSV or PXD, we can specify one experiment in one container.

### Container page
If you know the container ID, such as RMSV0000248, you can search in the main MassIVE webpage. Also you can access from the dataset, for example, MSV000079843 for this container.

**_todo : 1) new capture for whole page**
![](img/access_quant_reanalyses/datasetpage_show_container_iprg.png)


### Title

It shows the title that submitter provided in `Add Reanalysis Results` workflow. For this container, 'CCMS reanalyses for/from training activities'.


### Description

It shows the description that submitter wrote in `Add Reanalysis Results` workflow.


### Reanalyzed Datasets

It shows the datasets reanalyzed for this container. This container is belonged to this dataset. For this container, the reanalyses under this container are used the datasets from the data, MSV000079843. If you click the MSV ID, you will move to the dataset webpage.


### Active Reanalyses

At the bottom of this page, there is the table to show the list of reanalyses in this container. For this example, there are 28 reanalyses available in this container. Each reanalysis has RMSV ID with the suffix in the container RMSV ID. 


### Summary table for one reanalysis

There is the summary box on the left of this page. It shows the simple summary about experimental design and quantification/statistical analysis for this reanalysis.

**_todo : 2) new capture for summary table_**

1. **Experimental Design**: The summary of detected experimental design from `Metadata` category.

    - **Condition**: Number of distinct conditions across all reanalyses in this container. Distinct condition labels are counted across all files submitted in the `Metadata` category having a `Condition` column in this container's reanalyses. For this container, there are four conditions across all files in the `Metadata` category in this container's reanalyses.

    - **Biological Replicates**: Number of distinct biological replicates across all reanalyses in this container. Distinct replicate labels are counted across all files submitted in the `Metadata` category having a `BioReplicate` or `Replicate` column in this container's reanalyses. For this container, four unique IDs for biological replicates are available across all 'annotation.csv' files in the `Metadata` category in this container's reanalyses.

    - **Technical Replicates**: Number of distinct technical replicates across all reanalyses in this container. The technical replicate count is defined as the maximum number of times any one distinct combination of condition and biological replicate was analyzed across all files submitted in the `Metadata` category. In the case of fractionated experiments, only the first fraction is considered. For this container, maximum three technical replicates for the corresponding biological replicate are available across all reanalyses in this container.

2. **Identification Result**: The summary of the result for identification searching from `xx` category.

    - **Protein (Human, Remapped)**: Originally identified proteins that were automatically remapped by MassIVE to proteins in the SwissProt human reference database.
    
    - **Proteins (Reported)**: Number of distinct protein accessions reported by originally submitted search results.
    
    - **Peptides**: 
    
    - **Variant Peptides**:
    
    - **PSMs**: 

3. **Quantification Result**: The summary of the result for statistical analysis from `Statistical Analysis of Quantified Analytes` category.

    - **Differential proteins**: Number of distinct proteins found to be differentially abundant in at least one comparison across all reanalyses in this container. A protein is differentially abundant if its change in abundance across conditions is found to be statistically significant with an adjusted p-value <= 0.05 and lists no issues associated with statistical tests for differential abundance . Distinct protein accessions are counted across all files submitted in the `Statistical Analysis of Quantified Analytes` category having a `Protein` column in this container's active reanalyses. For this container, there are xx reanalyses including the table for the result of statistical analysis in the `Statistical Analysis of Quantified Analytes` category. Ten proteins are significantly different for at least one pairwise comparisons across xx reanalyses.

    - **Quantified proteins**: Number of distinct proteins quantified across all reanalyses in this container. Distinct protein accessions are counted across all files submitted in the `Statistical Analysis of Quantified Analytes` category having a `Protein` column in this container's active reanalyses. For this container, 2,875 proteins were quantified and tested by MSstats across xx reanalyses in this container.
    

### [Button : FTP Download](2_download_files.md)

All the submitted files in the reanalysis are available for downloading from FTP. See [here](2_download_files.md) for detailed instructions on how to download the files in any category.


### [Button : Browse Quantification Results](2_browse_files.md)

You can browse the quantification results for the reanalysis by clicking on **Browse Quantification Results** from the reanalysis page. See [here](2_browse_files.md) for detailed instructions on how to browse the files in the `Quantification Result` or `Statistical Analysis of Quantified Analytes` categories.


### [Button : Browse Metadata](2_browse_files.md)

You can browse the metadata for the reanalysis by clicking on **Browse Metadata** from the reanalysis page. See [here](2_browse_files.md) for detailed instructions on how to browse the files in the `Metadata` category.
