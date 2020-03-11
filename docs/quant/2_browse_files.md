
### Browse Metadata

You can browse the metadata for the reanalysis by clicking on **Browse Metadata** from the reanalysis webpage. This button is activated only when any tabular-type file(s) is available in the `Metadata` category.

![](img/access_quant_reanalyses/browse_metadata_step1.png)

You will move to the new webpage to show the list of files under the `Metadata` category.
![](img/access_quant_reanalyses/browse_metadata_step2.png)


Select one file name and it will show how the file looks. This is the example of an annotation file for MSstats, which requires *Run* or *Raw.file*, *Condition*, *BioReplicate*. It can have many additional columns.

![](img/access_quant_reanalyses/browse_metadata_step3.png)

You can filter the rows. Let's check the rows for 'Condition1'.

1. Type 'Condition1' in the empty box in the first row and below the column named 'Condition'.
2. Click `Filter` button at the top left of the table.

Then, the rows with 'Condition1' for `Condition` column are shown. For this example, there are three Runs from 'Condition1'.

![](img/access_quant_reanalyses/browse_metadata_filtered.png)

If you want to remove the filter and to see the whole table, remove 'Condition1' that you typed and click the same `Filter` button again.

**_!! Note_**: *Run* and *Raw.file* are identical in most datasets. However, if *Run* information in quantification files are different than the name of raw files, we recommend to provide both *Run* and *Raw.file* in the `Metadata`. *Raw.file* refers to the name of .raw file in the original submission of dataset. *Run* refers to MS run ID in the quantification files.


### Browse Quantification Results

You can browse the quantification results for the reanalysis by clicking on **Browse Quantification Results** from the reanalysis webpage. This button is activated only when any tabular-type file(s) is available in the `Quantification Results` or `Statistical Analysis of Quantified Analytes` categories.

![](img/access_quant_reanalyses/browse_quantresult_step1.png)

You will move to the new webpage to show the list of files under the `Quantification Results` or `Statistical Analysis of Quantified Analytes` categories.

Select one file, named _quant/Choi2017_DDA_Skyline_input.csv_. This file was submmited to the `Quantification Results`. 
![](img/access_quant_reanalyses/browse_quantresult_step2.png)


***Note***: The file size of the quantification result could be big. If the webpage shows like below, please wait for little more.
![](img/access_quant_reanalyses/browse_quantresult_wait.png)

This is the example of the quantification result (MSstats reports) from Skyline. 

![](img/access_quant_reanalyses/browse_quantresult_quant.png)

Let's see another file. Select one file, named _quant_stats/Choi2017_DDA_Skyline_testResult_byMSstats.csv_. This file was submitted to `Statistical Analysis of Quantified Analytes`. 
![](img/access_quant_reanalyses/browse_quantresult_step3.png)

This is the example of the output of MSstats, using the quantification result from Skyline (named _Choi2017_DDA_Skyline_input.csv_, the file shown above).
![](img/access_quant_reanalyses/browse_quantresult_stats.png)

You can filter the rows. Let's check the rows for a protein named 'sp|D6VTK4|STE2_YEAST'.

1. Type 'sp|D6VTK4|STE2_YEAST' in the empty box in the first row and below the column named 'Protein'.
2. Click the `Filter` button at the top left of the table.

Then, the rows with 'sp|D6VTK4|STE2_YEAST' for the `Protein` column are shown. There are six rows with different `Label`, which shows different pairwise comparisons. The user can customize the names of comparisons, which are shown in the `Label`, in MSstats. It can be different than the values of `Condition` in the annotation file. 

![](img/access_quant_reanalyses/browse_quantresult_filtered_protein.png)



If you want to remove the filter and to see the whole table, remove 'sp|D6VTK4|STE2_YEAST' that you typed and click the same `Filter` button again.


Let's check the rows with significantly different proteins and comparisons.

1. Type '0.5' in the second empty box in the first row and below the column named 'adj.pvalue'.
2. Type 'NA' in the empty box in the first row and below the column named 'issue'.
2. Click the `Filter` button at the top left of the table.

Then, the rows with significantly differential abundunce are shown. There are 29 rows shown. Among 29 rows, there are 7 unique proteins.

![](img/access_quant_reanalyses/browse_quantresult_filtered_sig.png)
