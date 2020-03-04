# Analysis of Post-Translational Modifications using CCMS tools

We use two different workflows for identification of modifications

* [Maestro workflow](workflows/maestro.md): identification of peptide-spectrum matches (PSMs) by i) spectral library search (MSPLIT) for detection of known reference peptides, followed by ii) restricted database search with known modifications (MSGF+), and finally followed by iii) open-modification search (MODa) for identification of peptides with unexpected modifications.
    * Maestro primarily identifies modified **peptide variants**: distinct pairs (S,M) where S is a peptide sequence and M is the summed mass of all 'delta-mass' modifications assigned on sequence S. This abstraction is required for proper control of false discovery rates at PSM and peptide levels in Maestro; the resolution of delta-masses into putative modifications and modification sites is done with ModDecode as described below.

* [ModDecode workflow](workflows/moddecode.md): post-processing of modified PSMs for i) resolution of delta-masses into known UniMod modifications for PSMs with unexpected modifications, ii) site assignment at fixed false localization rate and iii) calculation of AlignGF p-values between differently-modified versions of the same peptide.
    * ModDecode primarily identifies modified **peptidoforms**: peptide sequences with site-resolved modifications whose masses were matched to known UniMod entries for putative resolution into (possibly combinations of) known modifications or amino acid polymorphisms.

The following sections focus on different aspects of the analysis of modifications and modified peptides. All links below use two example jobs whose results will be reported soon: a [Maestro job](https://proteomics2.ucsd.edu/ProteoSAFe/status.jsp?task=de809a3717cc4d96a3a5257e290351d5) co-analyzing colon samples from the draft proteomes and a colon cancer dataset and the corresponding [ModDecode](https://proteomics2.ucsd.edu/ProteoSAFe/status.jsp?task=790e82c2ef1541748521db1e94b24fe0) job with resolved modifications and peptidoforms.

### Analyzing known modifications

1. Start with ModDecode list of [UniMod modifications](https://proteomics2.ucsd.edu/ProteoSAFe/result.jsp?task=790e82c2ef1541748521db1e94b24fe0&view=t_group_by_knownmod); the default sorting order is by decreasing number of distinct peptides identified with each modification. 
1. Additional important criteria for inspection of modifications:
    1.1. test sub-item in numbered lists 1
   

### Analyzing peptidoforms

### Analyzing hypermodified regions

### Analyzing putative novel modifications



