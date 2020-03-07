# Analysis of Post-Translational Modifications using CCMS tools

We use two different workflows for identification of modifications:

* [Maestro workflow](workflows/maestro.md): identification of peptide-spectrum matches (PSMs) by i) spectral library search (MSPLIT) for detection of known reference peptides, followed by ii) restricted database search with known modifications (MSGF+), and finally followed by iii) open-modification search (MODa) for identification of peptides with unexpected modifications.
    * Maestro primarily identifies modified **peptide variants**: distinct pairs (S,M) where S is a peptide sequence and M is the summed mass of all 'delta-mass' modifications assigned on sequence S. This abstraction is required for proper control of false discovery rates at PSM and peptide levels in Maestro; the resolution of delta-masses into putative modifications and modification sites is done with ModDecode as described below.

* [ModDecode workflow](workflows/moddecode.md): post-processing of modified PSMs for i) resolution of delta-masses into known UniMod modifications for PSMs with unexpected modifications, ii) site assignment at fixed false localization rate and iii) calculation of AlignGF p-values between differently-modified versions of the same peptide.
    * ModDecode primarily identifies modified **peptidoforms**: peptide sequences with site-resolved modifications whose masses were matched to known UniMod entries for putative resolution into (possibly combinations of) known modifications or amino acid polymorphisms.
***
The following sections focus on different aspects of the analysis of modifications and modified peptides. All links below use two example jobs whose results will be reported soon: a [Maestro job](https://proteomics2.ucsd.edu/ProteoSAFe/status.jsp?task=de809a3717cc4d96a3a5257e290351d5) co-analyzing colon samples from the draft proteomes and a colon cancer dataset and the corresponding [ModDecode](https://proteomics2.ucsd.edu/ProteoSAFe/status.jsp?task=790e82c2ef1541748521db1e94b24fe0) job with resolved modifications and peptidoforms.

### Analyzing known modifications

1. Start with ModDecode list of [UniMod modifications](https://proteomics2.ucsd.edu/ProteoSAFe/result.jsp?task=790e82c2ef1541748521db1e94b24fe0&view=t_group_by_knownmod); the default sorting order is by decreasing number of distinct peptides identified with each modification (**"#Pepts"**). 
1. Additional important criteria for inspection of modifications:
    * **"% Explained"** >= 0.5: filter for modifications with at least one PSM with >= 50% intensity explained by theoretical ions derived from the modified peptidoform sequence
    * **"MaxModFrags"** >= 2: filter for modifications with at least one PSM with >= 2 spectrum peaks assigned to modified ion fragments (exclude this filter for labile modifications)
    * **"PValue"** >= 10: filter for modifications with at least one PSM matching a differently-modified (e.g., unmodified) PSM of the same peptide with an AlignGF p-value <= 1e-10
    
Other considerations for the inspection of modifications

* The identification of a modification in a sample is only as good as the best PSM evidence that can be provided for that modification. See below for considerations for identification of modified peptidoforms.
* Different modifications can have very similar mass; for example, several modifications and amino acid polymorphisms have [integer mass of 14 Da](https://proteomics2.ucsd.edu/ProteoSAFe/result.jsp?task=790e82c2ef1541748521db1e94b24fe0&view=t_group_by_knownmod#%7B%22main.mass_lowerinput%22%3A%2214%22%2C%22main.mass_upperinput%22%3A%2214%22%7D) and very close or indistinguishable mono-isotopic masses.
* The same modification can occur on multiple different amino acids and sites: for example, the first 3 modified peptidoforms for peptide VGAHAGEYGAEALER [shown on this list](https://proteomics2.ucsd.edu/ProteoSAFe/result.jsp?task=790e82c2ef1541748521db1e94b24fe0&view=t_group_by_spectrum#%7B%22modFragNum_lowerinput%22%3A%222%22%2C%22calcPV_lowerinput%22%3A%2210%22%2C%22minRatio_lowerinput%22%3A%22.5%22%2C%22table_sort_history%22%3A%22curatedPept_asc%3BunmodPept_asc%3BminRatio_dsc%22%2C%22numMod_upperinput%22%3A%221%22%2C%22unmodPept_input%22%3A%22.VGAHAGEYGAEALER.%22%2C%22ModAnnotation_input%22%3A%22%2B16%2C%22%7D) localize the +15.995 Da mass offset to 3 different sites (once as an oxidation on Y and twice as polymorphisms of A to S, all resulting from the exact same change in elemental composition), each supported by multiple site-localizing b and y ions at mass error <= 10 ppm.

### Analyzing peptide variants and peptidoforms

Analyzing peptide variants
* First establish that it's the correct peptide - inspect the fragmentation pattern and compare it to that of related (possibly unmodified) variants of the same peptide
* (1) Copy input PSM string from ModDecode row and use it to filter Clusters view in Maestro and (2) click on the "Spectral networks" link to open the network
* (1a) Copy input PSM string from ModDecode row and use it to filter Spectral Networks view in Maestro + Click "Visualize Network" and (2) Label nodes with peptide strings and (3) Search for peptide string

Analyzing peptide modification masses
* Are there are other, higher-reliability modifications of similar mass identified on the same peptide? If yes, is there enough evidence to call an additional modification?
   - Example peptide [ATAASSSSLE+13.979K](https://proteomics2.ucsd.edu/ProteoSAFe/result.jsp?task=790e82c2ef1541748521db1e94b24fe0&view=t_group_by_spectrum#%7B%22Index_lowerinput%22%3A%221337854%22%2C%22Index_upperinput%22%3A%221337854%22%7D), with Carbonyl modification on E10; note mass of highest-intensity modified y-ion ion y7 at 751.35, matching the theoretical mass 751.347 with mass error < 5 ppm. Other modified y ion masses further confirm this assignment.
   - Example peptide [ATAASSSSLE+14.016K](https://proteomics2.ucsd.edu/ProteoSAFe/result.jsp?task=790e82c2ef1541748521db1e94b24fe0&view=t_group_by_spectrum#%7B%22Index_lowerinput%22%3A%221660252%22%2C%22Index_upperinput%22%3A%221660252%22%7D), with Methylation modification on E10; note mass of highest-intensity modified y-ion ion y7 at 751.387, matching the theoretical mass 751.387 with mass error < 5 ppm. Other modified y ion masses further confirm this assignment.

Analyzing modification sites
* Is the same modification (or a different modification of the same mass) identified elsewhere on the same peptide? If yes, are there enough site-assignment peaks between the two sites to call an additional modification site?
* Filter the PSMs view for **"DtFlrPeaks"** >= 2

### Analyzing hypermodified regions


### Analyzing putative novel modifications



