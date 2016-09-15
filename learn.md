<style>
  body {
    line-height: 2;
    font-family: "Helvetica";
  }
  hr {
    border-top: 3px solid #C0C0C0;
  }
</style>

# Tutorials and Protocols

The GVL project team have produced a number of tutorials and analysis protocols for:

*   Galaxy
*   GenomeSpace
*   Genomics Analysis

There are a combination of basic and advanced galaxy tutorials and command line tutorials which give step by step instructions for an example analysis. Protocols outline the analysis methods and suggest and compare tools for each step rather than prescribe them.

* * *

## Learn Galaxy

The tutorials listed here are designed to teach beginners how to use the Galaxy analysis platform. There are also a number of links to other resources from outside the GVL.

#### [Introduction to Galaxy](http://vlsci.github.io/lscc_docs/tutorials/galaxy_101/galaxy_101/)

*   A tutorial for those who are very new to Galaxy.

#### [Galaxy Workflows](http://vlsci.github.io/lscc_docs/tutorials/galaxy-workflows/galaxy-workflows/)

*   Using Histories and Workflows for those with some Galaxy knowledge.

#### Other Galaxy Resources

*   The Galaxy project website has any tutorials and screencasts about using Galaxy and the tools, and developing new tools.
    *   [Tutorials](http://wiki.galaxyproject.org/Learn)
    *   [Screencasts](http://wiki.galaxyproject.org/Learn/Screencasts)
*   [Queensland Facility for Advanced Bioinformatics](http://www.qfab.org/) training resources
*   [Victorian Life Sciences Computation Initiative](http://www.vlsci.org.au/lscc) training resources
*   Global resources of the [Galaxy Training Network](https://wiki.galaxyproject.org/Teach)

* * *

## Learn GenomeSpace

The tutorials listed here are designed to teach beginners how to use the GenomeSpace data storage platform.

#### [GenomeSpace](https://vlsci.github.io/lscc_docs/tutorials/genomespace/genomespace/)

*   A tutorial for anyone wanting to learn how to use the GenomeSpace Data Platform and how to interact with it from Galaxy and the rest of the GVL.

* * *

## RNA Seq

Measuring the state of a system by quantifying the amount of each messenger RNA present.

#### [Basic Galaxy Tutorial](http://vlsci.github.io/lscc_docs/tutorials/rna_seq_dge_basic/rna_seq_basic_tutorial/)

*   RNA-Seq tutorial based on [Trapnell et al. (2012) Nature Protocols](http://www.nature.com/protocolexchange/protocols/2327)
*   In this tutorial we cover the concepts of RNA-Seq differential gene expression (DGE) analysis using a very small synthetic dataset from a well studied organism.

#### [Advanced Galaxy Tutorial](http://vlsci.github.io/lscc_docs/tutorials/rna_seq_dge_advanced/rna_seq_advanced_tutorial/)

*   A more advanced RNASeq tutorial
*   In this tutorial we compare the performance of three statistically-based differential expression tools:
    *   CuffDiff
    *   EdgeR
    *   DESeq2

#### Advanced Command Line Tutorial

*   An advanced RNASeq tutorial using the linux commmand line.
*   Graphical Output with CummeRbund introduces some basic commands using the cummeRbund package of the R programming language. You will learn how to produce graphical output from RNA-Seq analysis previously done using a Cuffdiff analysis. You have three options for the required software installation (how to is explained in the Tutorial):
    *   [**On your PC**](https://docs.google.com/document/d/1ayJXtgBP1OXtnV7o7lq4QHKMNk5SdPHFq4hGkqndBtI/pub): You need to install R, RStudio and cummeRbund on your PC; and load the data onto your PC.
    *   [**On a Personal GVL**](https://docs.google.com/document/d/1ayJXtgBP1OXtnV7o7lq4QHKMNk5SdPHFq4hGkqndBtI/pub): You need to launch a Personal GVL; install cummeRbund; and load the data. This will avoid pitfalls you may experience when trying to install R and RStudio on your PC.
    *   [**On a Personal GVL linked to Galaxy**](https://docs.google.com/document/d/1ayJXtgBP1OXtnV7o7lq4QHKMNk5SdPHFq4hGkqndBtI/pub): You need to launch a Personal GVL; install cummeRbund; link to Galaxy and perform the RNA seq basic tutorial. This demonstrates advanced use of GVL, using RStudio to access Galaxy data.

* * *

## Variant Calling

Variant calling is the process of finding differences in your read data set from a reference sequence. It usually involves aligning sequences of your sample (be they reads or other) against a reference of your choosing, then searching for differences - be they SNPs, SNVs, CVs, InDels etc.

#### [Basic Galaxy Tutorial](http://vlsci.github.io/lscc_docs/tutorials/variant_calling_galaxy_1/variant_calling_galaxy_1/)

*   In this tutorial we cover the concepts of detecting small variants (SNVs and indels) in human genomic DNA using a small set of reads from chromosome 22.

#### [Advanced Galaxy Tutorial](http://vlsci.github.io/lscc_docs/tutorials/var_detect_advanced/var_detect_advanced/)

*   In this tutorial we compare the performance of two statistically-based variant detection tools:
    *   GATK: Unified Genotyper
    *   FreeBayes
*   Each of these tools takes as its input a BAM file of aligned reads and generates a list of likely variants in VCF format

#### Pipelines

Pipelines are for those who are comfortable with using the UNIX command line; and often allow more control over branching and iteration logic.

[**WGS/exome GATK-based variant calling pipeline**](https://github.com/claresloggett/variant_calling_pipeline)

*   This is a basic variant-calling and annotation pipeline developed at the Victorian Life Sciences Computation Initiative (VLSCI), University of Melbourne.
*   It is based around BWA, GATK and ENSEMBL and was originally designed for human (or similar) data.
*   The master branch is configured for WGS data; there is an exome branch configured for variant calling in exome data.
*   To run the pipeline you will need Rubra: [https://github.com/bjpop/rubra](https://github.com/bjpop/rubra). Rubra uses the python Ruffus library: [http://www.ruffus.org.uk](http://www.ruffus.org.uk/).

#### Protocols

[**Familial Variant Calling**](https://docs.google.com/document/d/1lfDYNzHjfDA1pHTHd-0w3xHhg7L4TipT1gRfzgiV8es/pub)

*   In this protocol we discuss and outline the process of calling familial related mutations.

[**Somatic Variant Calling**](https://docs.google.com/document/d/1PIhm8NrFGaSK0hxpDcp8wUOz11ZkOaHIrpnJshMgDec/pub)

*   In this protocol we discuss and outline the process of identifying somatic variants or mutations.

* * *

## Assembly

Assembly is the process of taking DNA sequence data in the form of reads and reconstructing likely large contiguous segments of the original DNA. Presented here are an example Galaxy tutorial for the assembly of an E.coli genome from some Illumina sequence data and also a more generic assembly protocol document.

####[Basic Galaxy Tutorial](http://vlsci.github.io/lscc_docs/tutorials/assembly/assembly/)

* In this tutorial we carry out de novo assembly of a microbial genome.
* We have also written a De novo Genome Assembly for Illumina Data Protocol, for a more generic description of the method.

####[Assembly Protocol](http://vlsci.github.io/lscc_docs/tutorials/assembly/assembly-protocol/)

* De novo Genome Assembly for Illumina Data
* In this protocol we discuss and outline the process of de novo assembly for small to medium sized genomes.
* Use our Genome assembly tutorial to learn a specific case of using Galaxy to carry out de novo assembly of a microbial genome.

* * *

## ChIP-Seq

[Background material](https://docs.google.com/document/d/1FPmKuUZ-mgIT88E_uhs66QckwKcf5f_K49Zfg6SCB4s/pub): ChIP-Seq, or ChIP-sequencing, is an approach used for analysis of protein binding sites in genomes. It utilises chromatin immunoprecipitation (ChIP) and high-throughput sequencing technology.

####[Basic Galaxy Tutorial](https://docs.google.com/document/d/12pTphYcSUNnlorQWHBWo2LwxHGdZzR5Pxa5IjFkIHHk/pub)

* Introduction to ChIP-Seq analysis
* We cover the concepts of chromatin immunoprecipitation followed by massively parallel sequencing using a small subset of data obtained in mouse cell culture.

####[Advanced Galaxy Tutorial](https://docs.google.com/document/d/1KyHPoD6X_u3KfHCZuBlgNOaZmo7Tob2q-JdujhkF06Q/pub)

* ChIP-Seq and discovery of motifs This tutorial includes:
  * Peak calling using MACS2 with experimental and control datasets (CTCF ChIP-Seq data from mouse cell line)
  * Data exchange between Galaxy and UCSC Table Browser
  * Prediction of a nucleotide motif (a binding site consensus for CTCF protein) in sequences from the identified peak regions using MEME software.

####[ChIP-Seq Protocol](https://docs.google.com/document/d/1UPJC8dsiDeP5R9MH9U0IvoDgPF2Q3EOstAuzS3e6WCE/pub)

* In this protocol we discuss ChIP-Seq: a method to analyze the interaction between proteins and DNA.

* * *

## Metagenomics

Metagenomics is the study of genetic material recovered directly from environmental samples. While traditional microbiology and microbial genome sequencing and genomics rely upon cultivated clonal cultures, early environmental gene sequencing cloned specific genes (often the 16S rRNA gene) to produce a profile of diversity in a natural sample. Presented here is a Galaxy tutorial of an example 16S RNA analysis.

####[16S rRNA Analysis Galaxy Tutorial](https://docs.google.com/document/d/1A5xShJpmS97LY8jV5p1buVDHzx_BqJIe3mkfZrTCETQ/pub)

* In this tutorial we cover the concepts of metagenomics analysis in 16S rRNA.

* * *

## Amplicons

####[Amplicon Alignment Protocol](https://docs.google.com/document/d/1uW7JzxG86QzS92hTyeuNsLhX_d1XFbaZPSjh7jWxcSg/pub)

* In this protocol we discuss and outline the process of aligning custom amplicons using primers for high precision.
