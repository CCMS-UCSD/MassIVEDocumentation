## Step 2: Add Reanalysis workflow for quantification data

Once your files are fully uploaded to your user account directory at MassIVE, then you must run the **Add Reanalysis** workflow on those files in order to submit your dataset as reanalysis in the dataset (under MSV).


### Select Dataset

First, go to the webpage for the dataset you reanalyzed. You can search dataset MSV ID or PXD ID in [dataset's web page](../access_public_datasets.md#MassIVEDatasetBrowsing-ViewingaDataset).

click the **Add Reanalysis** button:

<center>
![](img/submit_quant_reanalyses/add_reanalysis_button_iprg.png){width=60%}
</center>


### Workflow Selection and Reanalysis Metadata Sections

**Add Reanalysis** button brings you to a MassIVE reanalysis attachment workflow input form.
Automatically, **'MassIVE Dataset: Add Reanalysis Results'** should be selected in `Workflow`. `Species`, `Instrument`, `Post-Translation Modifications` should be filled automatically from original submission. You should add 

1. the title in `Title` (at least 30 characters)
2. the description for this reanalysis in `Description` (at least 50 characters).


<center>
![](img/submit_quant_reanalyses/add_title_description_iprg.png){width=75%}
</center>

For example, 'MassIVE.quant reanalysis from offline MaxQuant+MSstats results' can be the `Title`. The short summary about the steps for reanalysis can be the `Description`, like 'MassIVE.quant reanalysis of data from the iPRG2015 study (dataset MSV000079843) using Andromeda for identification and MaxQuant for quantification, followed by MSstats for statistical analysis of differentially abundant proteins.'


### Reanalysis File Selection section 
You should select all the files for your reanalysis by clicking any of **Select Input Files** buttons:

<center>
![](img/submit_quant_reanalyses/add_reanalysis_file_iprg.png){width=75%}
</center>


Then, file selection window should be popped up. The file selection pop-up window (below) browses your account to select the files you uploaded, as well as any other files you wish to attach for this reanalysis. You should find that the proper dataset is automatically imported to your account from when you clicked "Add Reanalysis" back on the dataset page. You can see that Raw spectrum files and Peak list files which are available in MSV are already selected. At least one of Raw spectrum files from the original MSV should be selected to link this reanalysis with the original dataset.


<center>
![](img/submit_quant_reanalyses/file_selection_popup_iprg_full.png){width=70%}
</center>


#### Select reanalysis files (The most important steps!!)
Then you can select valid reanalysis files in this step. Please choose the proper file selection. Here are more help on each of individual categories for quantification and statistical analysis results.


| Category                                     | Notes                                                                                    |
| -------------------------------------------- | ---------------------------------------------------------------------------------------- |
| Quantification results                       | Quantification result files from data processing tools/quantification tools. It should be used for downstream statistical analysis. For example, PSM-level or transition-level or protein-level quantified peak intensities data should be in this category.  |
| Metadata                                     | Information about design of experiments should be submitted in Metadata section. For example, annotation file for MSstats should have the information about biological replicate, technical replicate, fraction, condition or group for the corresponding MS runs and corresponding channels. |
| Statisitical analysis of quantified analytes | Result files for statistical analysis. It could be the table or figure of result for statistical analysis. For example, table (.txt, .csv), r data format for differential abundance analysis or pdf for figures can be saved in this section. |
| Supplementary                                | Any other type of information. For example, the software-specific files from processing software can be shared in this section (sky, skyd, sky.zip, blib, irtdb, protdb, optdb, and midas for Skyline, .pdresult for Proteome Discoverer, .sne for Spectronaut).|

#### Examples : input and output using MSstats for differential abundance analysis

Here are the examples of quantification files and the output of MSstats for statistical analysis and their corresponding categories to submit.

| Data processing tool | File type                | File Selection Category                     |
| -------------------- | ------------------------ | ------------------------------------------- |
| All                  | input.csv                | Quantification results                      |
|                      | annotation.csv           | Metadata                                    |
|                      | testResult_byMSstats.csv | Statistical analysis of quantified analytes |
|                      | msstats.log              | Methods and protocols                       |
|                      | Rscript.R                | Methods and protocols                       |
|                      | Description.pdf          | Methods and protocols                       |
| MaxQuant             | evidence.txt             | Quantification results                      |
|                      | proteinGroups.txt        | Quantification results                      |
|                      | parameters.txt           | Quantification results                      |
|                      | mqpar.xml                | Methods and protocols                       |
|                      | fasta                    | Sequence database                           |
| Spectronaut          | input.xls                | Quantification results                      |
|                      | SpectronautAnalysis.sne  | Supplementary files                         |
| DIA-Umpire           | FragSummary.xls          | Quantification results                      |
|                      | PeptideSummary.xls       | Quantification results                      |
|                      | ProtSummary.xls          | Quantification results                      |
| OpenSWATH            | input.tsv or input.txt   | Quantification results                      |
| Skyline              | .sky.zip                 | Supplementary files                         |


#### How to select file and selection
**!! new capture with number of selection**



Once you've selected valid reanalysis files and proper categories, click "finish selection" buttons. You will be back to reanalysis attachment workflow input form.

<center>
![](img/submit_quant_reanalyses/file_selection_popup_done_iprg.png)
</center>

### Reanalysis Container Selection section

The reanalysis attachment workflow will determine which source datasets were reanalyzed, and will then prepare what's referred to as a "reanalysis container" for your attachment. A reanalysis container simply refers to the unique set of datasets that were reanalyzed - usually only one, but possibly more. The workflow then attaches your results to this container. Any other reanalysis results attached (by any user) to this same set of datasets will also go in the same container.

For example, `Reanalysis Container` shows all containers for the source dataset. You can choose one of them or make **New reanalysis container**. If you select 'New reanalysis container', then you should put the title for this container in `Reanalysis Container Title`.

<center>
![](img/submit_quant_reanalyses/reanalysis_container_iprg.png){width=75%}
</center>

### Mapping Spectrum Files to Identfication Files section

If you submitted new identification files, you should [map your result files to the dataset's peak list files](../submission_workflow.md#MassIVEDatasetSubmission-MappingPeakListandResultFiles).


### Workflow Submission section

Finally, you are ready to submit. Please type your email to get progress notice and click 'submit' buttom.

<center>
![](img/submit_quant_reanalyses/workflow_submission_done_iprg.png){width=75%}
</center>
