# Analysis of Post-Translational Modifications using CCMS tools

We use two different workflows for identification of modifications

* [Maestro workflow](workflows/maestro.md): identification of peptide-spectrum matches (PSMs) by i) spectral library search (MSPLIT) for detection of known reference peptides, followed by ii) restricted database search with known modifications (MSGF+), and finally followed by iii) open-modification search (MODa) for identification of peptides with unexpected modifications.
** Maestro primarily identifies modified peptide **variants**: distinct pairs (S,M) where S is a peptide sequence and M is the summed mass of all 'delta-mass' modifications assigned on sequence S. This abstraction is required for proper control of false discovery rates at PSM and peptide levels in Maestro; the resolution of delta-masses into putative modifications and modification sites is done with ModDecode as described below.

* [ModDecode workflow](workflows/moddecode.md): post-processing of modified PSMs for i) resolution of delta-masses into known UniMod modifications for PSMs with unexpected modifications, ii) site assignment at fixed false localization rate and iii) calculation of AlignGF p-values between differently-modified versions of the same peptide.



### Analyzing modifications

### Analyzing variants

