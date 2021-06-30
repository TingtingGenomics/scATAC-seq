# <h1 align="center">10X genomics scATAC-seq Library Construction</h1>

## Barcoding

[citation:Chromium Next GEM Single Cell ATAC Reagent Kits v1.1, 10X genomics, users guide.](https://assets.ctfassets.net/an68im79xiti/2NEwsG0Yu3RuxvtQiWXZo3/1e939394fa43a4f0bd88d79383833b16/CG000209_Chromium_NextGEM_SingleCell_ATAC_ReagentKits_v1.1_UserGuide_RevE.pdf)

This step synthesizes top single strands.

<p align="center">
<img width="50%" height="50%" src="library_barcoding.png">
</p>

***
**Notes:**
scATAC-seq sequencing constructs don't have UMI sequence because it's a DNA sequencing methods, not like RNA sequencing that contain many RNA transcripts to differentiate.![image](https://user-images.githubusercontent.com/31963567/124014533-a4aa6000-d9b1-11eb-83cf-0d274d784cea.png)
***

## Library Construction

## Sequencing





**Assay for Transposase-Accessible Chromatin Sequencing (ATAC-Seq)** employs a hyperactive form of Tn5 transposase to identify regions of open chromatin, which are important for global epigenetic control of gene expression. Tn5 simultaneously cleaves and adds adapters to nucleosome-free regions of DNA, priming them for sequencing.
<br />
<br />

<p align="center">
<img width="50%" height="50%" src="Tn5.vs.chromatin.png">
</p>

[citation:biomedcentral](https://hereditasjournal.biomedcentral.com/articles/10.1186/s41065-019-0105-9)

***
**Qestions:**
Could the cutting site of Tn5 span more than 0 nucleosome?
***
 
## How does Tn5 cut?
Each transposition creates a 9bp duplication, this is the reason that the genomic position of the sequenced fragments was adjusted 5 or 4bp to get the center point of the cutting site.

<p align="center">
  <img width="75%" height="75%" src="Tn5.cut1.jpeg">
</p>
<p align="center">
  <img width="75%" height="75%" src="Tn5.cut2.jpeg">
</p>

***
**Qestions:**
How to locate the exact cutting site of Tn5?
***

[citation:10X genomics](https://support.10xgenomics.com/single-cell-atac/software/pipelines/latest/output/fragments)
“The start of the interval is moved forward by 4bp from a left-most alignment position and backward 5bp from the right-most alignment position. The transposase cuts the two DNA strands with a 9bp overhang, and adjusted positions represent the center point between these cuts; this position is recorded as a cut site that represents a chromatin accessibility event.”

## Construct of equencing fragment after Tn5
<p align="center">
  <img width="50%" height="50%" src="Tn5_seq_fragment.jpeg">
</p>
[citation:abpbio](https://www.abpbio.com/product/tn5-transposase/)

