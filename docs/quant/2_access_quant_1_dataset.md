

Once the attachment job is finished, both the container and the reanalysis will now show up on the dataset page:

**_todo : 1) new capture for whole page**
![](img/access_quant_reanalyses/datasetpage_show_list_reanalysis_iprg.png)

title, description. there are some containers and reanalyses.

**_todo : 2) new capture for summary table**
Owner column

Reanalysis column


experimental design part : Condition, Bioreplicate, TechReplicate part

- **Condition**: Number of distinct conditions across all analyses (original submission and reanalyses) associated with this dataset. Distinct condition labels are counted across all files submitted in the `Metadata` category having a `Condition` column in this dataset.

- **Biological Replicates**: Number of distinct biological replicates across all analyses (original submission and reanalyses) associated with this dataset. Distinct replicate labels are counted across all files submitted in the `Metadata` category having a `BioReplicate` or `Replicate` column in this dataset.

- **Technical Replicates**: Number of distinct technical replicates across all analyses (original submission and reanalyses) associated with this dataset. The technical replicate count is defined as the maximum number of times any one distinct combination of condition and biological replicate was analyzed across all files submitted in the `Metadata` category. In the case of fractionated experiments, only the first fraction is considered.


Quantification Result part :

- **Differential proteins**: Number of distinct proteins found to be differentially abundant in at least one comparison across all analyses (original submission and reanalyses) associated with this dataset. A protein is differentially abundant if its change in abundance across conditions is found to be statistically significant with an adjusted p-value <= 0.05 and lists no issues associated with statistical tests for differential abundance. Distinct protein accessions are counted across all files submitted in the `Statistical Analysis of Quantified Analytes` category having a `Protein` column in this dataset.

- **Quantified proteins**: Number of distinct proteins quantified across all analyses (original submission and reanalyses) associated with this dataset. Distinct protein accessions are counted across all files submitted in the `Statistical Analysis of Quantified Analytes` category having a `Protein` column in this dataset.


### [Button : FTP Download](2_download_files.md)

All the submitted files in the reanalysis are available for downloading from FTP. See [here](download_files.md) for detailed instructions on how to download the files in any category.


### [Button : Browse Quantification Results](2_browse_files.md)

You can browse the quantification results for the reanalysis by clicking on **Browse Quantification Results** from the reanalysis page. See [here](browse_files.md) for detailed instructions on how to browse the files in the `Quantification Result` or `Statistical Analysis of Quantified Analytes` categories.


### [Button : Browse Metadata](2_browse_files.md)

You can browse the metadata for the reanalysis by clicking on **Browse Metadata** from the reanalysis page. See [here](browse_files.md) for detailed instructions on how to browse the files in the `Metadata` category.
