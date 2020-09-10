
### MassIVE.quant : Level of curation

In order to ensure the reproducibility of a quantitative workflow, MassIVE.quant maintains with four levels of curation, reflecting the documentation and the reproducibility of the quantitative workflow.

### Level 1. Bronze (Automatic review) 

During the submission, the infrastructure checks whether the submission of the dataset or reanalysis meets the minimal requirements for the entry-level (Bronze) of curation.

* Check ‘Metadata’ includes the required column headers : Condition, BioReplicate, Run (or Raw.files)
* Check whether the raw files in metadata are available in ‘raw spectrum files’ collection or not.
* Check any files in ‘Quantification’ collection
* Check any files in ‘Statistical Analysis of Quantified Analytes’ collection

If the submitted dataset or analysis meets the requirements above, then it will get the Bronze level. The submitter can then request the advanced review to level up.

###  Level 2. Silver (Manual review)

As a request from the submitter for Bronze level dataset or reanalysis, MassIVE team will review the submitted files related to quantification. If the submitted dataset or analysis meets the requirements below, then it will get the Silver level. 

* Metadata 
    * Summary statistics in the blue box are correct or not.
    * Correctly annotated for biological replicate. 
    * Correctly reported technical replicate and fraction.
    * More information is optional.

* Quantification 
    * Feature-level or protein-level quantification is available or not.
    * File can be parsed and showed up for browsing or not. For example, xls file with multiple sheets can not be parsed.

* Statistical Analysis of Quantified Analytes
    * Check whether it is meaningful information or not.  
    * Files can be parsed and showed up for browsing or not. For example, xls file with multiple sheets can not be parsed.
    * **!! Note** : it does not need to be the MSstats output format.

###  Level 3. Gold (Manual review) : Silver + Check repeatability

Mainly, Gold level means that anyone can repeat the same conclusion in ‘Statistical Analysis of Quantified Analytes’s collection, which requires more information about all data analysis steps.

As a request from the submitter for Silver level dataset or reanalysis, MassIVE team will review the submitted files related to quantification. If the submitted dataset or analysis meets the requirements below, then it will get the Gold level. 

* mqpar.xml, parameter files for MaxQuant -> Method collection
* Log files for MSstats -> Method collection
* R script or any script is available to reproduce statistical analysis.
* Tool-specific files including these information as alternatives, such as .pdresult, .pdstudy, .sne, .sky and so on.
* Or other configuration file to repeat the same analysis
* **!! Note** : Gold level doesn’t mean to reproduce the same conclusion in the original publication.
* **!! Note** : We don’t review or evaluate the method itself.

###  Level 4. Platinum (Manual review) : Gold + Check reproducibility for publication 

Platinum level means that anyone can reproduce the same conclusion in the publication. For example, the dataset or reanalysis fully documented for all data analysis steps will get the Platinum level.

As a request from the submitter for Gold level dataset or reanalysis, MassIVE team will review the submitted files related to quantification. If the submitted dataset or analysis meets the requirements below, then it will get the Platinum level. 

* The dataset (MSV) or reanalysis (RMSV) can be referred for the publication. Please don't forget to add publication in the description.
* **!! Note** : We don’t review or evaluate the method itself.

### FAQ: If you want to move your data in PRIDE to MassIVE?

Please let us(ccms-web@cs.ucsd.edu) know which datasets (PXD ID) to import and we'll get them to MassIVE for you.

### FAQ: How to request to review my submission to MassIVE.quant?

Please let us(ccms-web@cs.ucsd.edu) know MSV ID for dataset and RMSV ID for reanalysis and we'll get them to MassIVE for you.


### Online-office hours (help sessions)

If you are ready to submit data, reanalyses, or metadata to MassIVE.quant, but have difficulties or questions, we are happy to review your list of files and submit them together. Please apply through this [link](https://forms.gle/Ebj86Z2xTquuzzn18).
