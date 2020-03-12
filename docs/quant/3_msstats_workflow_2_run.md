
Once your files are fully uploaded to your user account directory at MassIVE or you know which MSV or RMSV has quantification file you want to reanalyze, you are ready to run **MSstats workflow** in MassIVE.quant.

### 2.1 Workflow Selection

First, go to the main webpage for [MassIVE](https://massive.ucsd.edu/ProteoSAFe/static/massive.jsp). Click **Submit your data** in the `Submit Data` section. 

<center>
![](img/run_msstats_workflow/msstats_workflow_step0.png)
</center>

It brings you to the workflow input form. Select **MSstats** from the drop-down button in the `Workflow`. Then the webpage will be changed as below. You should add the title in the `Title` (at least 30 characters).

<center>
![](img/run_msstats_workflow/msstats_workflow_step1.png)
</center>


### 2.2 File Inputs

You can reanalyze either your new quantification file(s) or published quantification file(s).  If you have new quantification files to analze by MSstats, please go to the section 2.2.1. If you want to use the published quantification file, please go to the section 2.2.2

#### 2.2.1 Option1: New Quant files

If you have new quantification files, then:
    
1. Select the name of the data processing tool you used from the drop-down button in the `Tool name`.
2. Select the files from your user account directory at MassIVE by clicking any of **Select Input Files** buttons:

<center>
![](img/run_msstats_workflow/msstats_workflow_file_input_newfile.png)
</center>

Next, the file selection pop-up window (below) helps you browses your account to select the files you uploaded. For **MSstats workflow**, `Annotation File` and `Features` are required to have any file.

Let's select `Annotation File` first.

1. Select the file in your account: *'Choi2017_DDA_MaxQuant_annotation.csv'* is the annotation file for this experiment. Select/Click the file name. Then, the file name will be highlighted.
2. Select category: At the top-left corner, there are boxes for categories. Select/Click the box named `Annotation File`.
3. Then, on the right panel, named `Selected Files`, you can see the selected file under the folder named `Selected Annotation File`.

Please repeat for quantification file(s). Most data processing tools report one feature-level quantified data, which is required for MSstats. It should be selected for the `Feature` category. For `MaxQuant` output, MSstats requires two quantification reports, `evidence.txt` for `Features` and `proteinGroups.txt` for `Proteins`. Repeat to select those two files in the corresponding category.

<center>
![](img/run_msstats_workflow/msstats_workflow_file_selection_popup_final.png)
</center>

Once you've selected valid annotation and quantification files in the proper categories, clicks the **Finish Selection** button.

<center>
![](img/run_msstats_workflow/msstats_workflow_file_input_done.png)
</center>


#### 2.2.2  Option2: Published Quant files

If you use the published quantification files, select the name of data processing tool you used from the drop-down button in the `Tool name`. Next, you should select the quantification and annotation files from the published datasets.

1. Click '**+**' sign in front of **Select Input Files from MassIVE dataset** option. Then, the list of dataset will be shown.
2. Type MSV ID in the empty box in the first row and below the column named 'Dataset', for example, 'MSV000079843'
3. Click the `Filter` button at the top left of the table. Then, the row with MSV ID your typed for the `Dataset` column is shown. 
4. Click the `Reanalyses` button at the very right.

<center>
![](img/run_msstats_workflow/msstats_workflow_file_input_fromdataset_step1.png)
</center>

Then, the `Dataset Reanalysis Selection` pop-up window helps you select the reanalysis, including the annotation and quantification files. Find the reanalysis, including the annotation and quantification files. If there are more than 5 reanalyses in the datasets, please use a double arrow (<< or >>) to see more reanalyses. Click the `Select` button at the very right in the row for the reanalysis you want.

<center>
![](img/run_msstats_workflow/msstats_workflow_file_input_fromdataset_step2.png)
</center>

Then, the new pop-up window, `File Selection`, shows all files in this reanalysis. Let's select the annotation file.

1. Find the annotation file. For this example, _Choi2017_DDA_MaxQuant_annotation.csv_ is the annotation file that we want to use. 
2. Select **Annotation File** from the drop-down button in the `Select` column.
3. Click the `Add` button at the very right.

<center>
![](img/run_msstats_workflow/msstats_workflow_file_input_fromdataset_step3.png)
</center>

Let's select the quantification files. For MaxQuant, two files should be selected : `evidence.txt` for `Features` and `proteinGroups.txt` for `Proteins`. Select both of them as below. Most data processing tools report one feature-level quantified data, which is required for MSstats. It should be selected for the `Feature` category.

<center>
![](img/run_msstats_workflow/msstats_workflow_file_input_fromdataset_step4.png)
</center>

Finally, click the `Close` button at the bottom-right on the pop-up window. Now, you can see three files are selected in total.

<center>
![](img/run_msstats_workflow/msstats_workflow_file_input_fromdataset_done.png)
</center>


### 2.3 Comparison Setup
Next, you should set up the comparison(s) between conditions of interest. The **MSstats workflow** provides four options to select comparions. You should choose one of them.

- **All vs. All**: This option will generate all pairwise comparisons between conditions in the annotation file. If there are four conditions in the annotation files (Condition1, Condition2, Condition3, Condition4), a total of six pairwise comparisons will be considered in MSstats : _Condition1-Condition2, Condition1-Condition3, Condition1-Condition4, Condition2-Condition3, Condition2-Condition4, Condition3-Condition4_.

<center>
![](img/run_msstats_workflow/msstats_workflow_contrast_all.png)
</center>

- **One vs. All**: This option will generate all pairwise comparisons between one selected condition (base condition) and other conditions in the annotation file. You should select the base condition from the drop-down button, next to `One vs. All` option. If there are four conditions in the annotation files (Condition1, Condition2, Condition3, Condition4) and you select _Condition1_ for the base condition, total three pairwise comparisons will be considered in MSstats : _Condition2-Condition1, Condition3-Condition1, Condition4-Condition1_.

<center>
![](img/run_msstats_workflow/msstats_workflow_contrast_one.png)
</center>

- **Choose Pairs**: This option will allow you to select any pairwise comparison(s) you want. If you select `Choose Pairs` option, the list of conditions will be shown. Select one condition per each panel and then select the `Add Selected Condition Pair` button. Then the comparison(s) you selected will be shown in the box below.

<center>
![](img/run_msstats_workflow/msstats_workflow_contrast_choose.png)
</center>

- **Contrast Matrix**: If you want to compare the complex linear combination between conditions, you can make your contrast matrix and use it for MSstats. The table for the contrast matrix can be saved as a txt file. It should be uploaded in your account directory at MassIVE.

<center>
![](img/run_msstats_workflow/msstats_workflow_contrast_attach.png)
</center>


### 2.4 Advanced options

There are advanced options for options available. This step is optional. The detailed information about all options is available in [msstats.org](http://msstats.org/msstats-2/).

<center>
![](img/run_msstats_workflow/msstats_workflow_adv_opt.png)
</center>

- Advanced Filtering Options: The options for converter functions in MSstats. `filter_with_Qvalue` or `proteinID` for many converter functions.
- Advanced Data Processing Options: The options of imputation and normalization in `dataProcess` function.
- Advanced Normalization Options: The option for `normalization='globalstandards` in `dataProcess` function.
- Advanced Feature Selection Options: This is for the options, `featureSubset` and `remove_uninformative_feature_outlier` in `dataProcess` function


### 2.5 Workflow Submission section

Finally, you are ready to submit. Please type your email to get progress notice and click **Submit** button.

<center>
![](img/submit_quant_reanalyses/workflow_submission_done_iprg.png)
</center>


Then, you will move to the new page, which shows the progress. Please wait. It will take a few minutes (or a few hours). After the job is done, you will get the notification email. The job done will be saved in your account at MassIVE.

<center>
![](img/run_msstats_workflow/msstats_workflow_job_done.png)
</center>


