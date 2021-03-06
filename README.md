### Herpes-Project-1 "Project 1: Incident HSV-2 and genital health in Kenyan adolescent girls: an inception cohort"
Code for analysis of vaginal explant microarray data

###Project outline
We infected vaginal biopsy explants from 7 donors with two strains of HSV-2 (SD90 and V186). We also did a Mock infection on an explant from each donor. In the code, these treatments are refered to at SD90, V186 and Mock. Donors are identified by a unique 3 digit TissueID.

RNA was isolated from the explants at 3 timepoints after infections: 3 hours, 8 hours and 24 hours. In the code, results from treatment and timepoint conditions are specified as treatment.timepoint (ex. V186.3 is the V186 treatment at the 3hr post infection timepoint).

We used the xxxx kit to extract and purify the RNA. RNA was sent to the FHCRC genomics (??) core facility to be spotted on Illumina Human HT12 v4 beadchip arrays. Samples (one sample is a single TissueID x Treatment x Timepoint) were named with random numbers from 6-69. 

A companion study using the same scheme but with immortalized lines of primary vaginal epithelial cells from three donors is documented elsewhere.

###Data analysis
R version 3.1.2 (2014-10-31)
lumi_2.18.0
Biobase_2.26.0
BiocGenerics_0.12.1
limma_3.22.7

#Workflow
*lumi: read in raw data, background correct, VST transform, robust spline normalize, QC
*Filter by detection p values
*limma: create model matrix and contrasts matrix, fit models to probes.
