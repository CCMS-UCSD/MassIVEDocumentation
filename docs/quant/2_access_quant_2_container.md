
As well as on the page for the container itself (which is always accessible from the dataset):

What the container is : xxx
If there are multiple experiments in one MSV or PXD, we can specify one experiment in one container.

**_todo : 1) new capture for whole page**
![](img/access_quant_reanalyses/datasetpage_show_container_iprg.png)

title, description. there are some reanalyses.

**_todo : 2) new capture for summary table**
experimental design part : Condition, Bioreplicate, TechReplicate part

- **Condition**: Number of distinct conditions across all reanalyses in this container. Distinct condition labels are counted across all files submitted in the “Metadata” category having a "Condition" column in this container's reanalyses

- **Biological Replicates**: Number of distinct biological replicates across all reanalyses in this container. Distinct replicate labels are counted across all files submitted in the “Metadata” category having a "BioReplicate" or "Replicate" column in this container's reanalyses.

- **Technical Replicates**: Number of distinct technical replicates across all reanalyses in this container. The technical replicate count is defined as the maximum number of times any one distinct combination of condition and biological replicate was analyzed across all files submitted in the “Metadata” category. In the case of fractionated experiments, only the first fraction is considered.

Quantification Result part :

- **Differential proteins**: Number of distinct proteins found to be differentially abundant in at least one comparison across all reanalyses in this container. A protein is differentially abundant if its change in abundance across conditions is found to be statistically significant with an adjusted p-value <= 0.05 and lists no issues associated with statistical tests for differential abundance . Distinct protein accessions are counted across all files submitted in the “Statistical Analysis of Quantified Analytes” category having a "Protein" column in this container's active reanalyses.

- **Quantified proteins**: Number of distinct proteins quantified across all reanalyses in this container. Distinct protein accessions are counted across all files submitted in the “Statistical Analysis of Quantified Analytes” category having a "Protein" column in this container's active reanalyses.