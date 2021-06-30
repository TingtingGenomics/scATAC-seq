# <h1 align="center">Cellranger-atac convert bcl file to fastq file</h1>

# Interpretation of bcl to fastq algorithm
[my previous notes](https://github.com/TingtingSsl2/scRNA-seq_LearningPage/blob/main/03_Convert%20bcl%20to%20fastq.md)

# Practice: convert bcl to fastq
[10X genomics](https://support.10xgenomics.com/single-cell-atac/software/pipelines/latest/using/mkfastq)

***
**Guildlines to download sample files from 10X genomics** 
- Download the tiny-bcl tar file.
- Untar the tiny-bcl tar file in a convenient location. This will create a new tiny-bcl subdirectory.
- Download the simple CSV layout file: cellranger-atac-tiny-bcl-simple-1.0.0.csv.
- Download the Illumina® Experiment Manager sample sheet: cellranger-atac-tiny-bcl-samplesheet-1.0.0.csv.
***

1. Login to BWH supercomputing system ERISONE, which has cellranger-atac installed under request. Locate to the working dir. 
```
cd /data/bioinformatics/projects/scATAC
```

2. Load modules required for scATAC-seq analysis. 
```
module load cellranger-atac/2.0.0
module load bcl2fastq2/default # this version works
```

3. 
```
cellranger-atac mkfastq \
--id=tiny-bcl \
--run=/data/bioinformatics/projects/scATAC/cellranger-atac-tiny-bcl-1.0.0 \
--csv=cellranger-atac-tiny-bcl-simple-1.0.0.csv
