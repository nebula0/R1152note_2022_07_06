#paper_from_adviser 

This article is great and important but i haven't finished. 2022_7_5

## note
> ### genome available or not
>  if a genome sequence is available for the studied organism, it should be possible to identify transcripts by mapping RNA-seq reads onto the genome. By contrast, for organisms without sequenced genomes, quantification would be achieved by first assembling reads de novo into contigs and then mapping these contigs onto the transcriptome.

> ![](attachment/Pasted%20image%2020220705141903.png)

> ### strand-specific  
> Several strand-specific protocols [[2](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-016-0881-8#ref-CR2 "Levin JZ, Yassour M, Adiconis X, Nusbaum C, Thompson DA, Friedman N, et al. Comprehensive comparative analysis of strand-specific RNA sequencing methods. Nat Methods. 2010;7:709–15.")], such as the widely used dUTP method, extend the original protocol by incorporating UTP nucleotides during the second cDNA synthesis step, prior to adapter ligation followed by digestion of the strand containing dUTP

> ### SE
> The cheaper, short SE reads are normally sufficient for studies of gene expression levels in well-annotated organisms, whereas longer and PE reads are preferable to characterize poorly annotated transcriptomes

> ### sequence depth
> Another important factor is sequencing depth or library size, which is the number of sequenced reads for a given sample. More transcripts will be detected and their quantification will be more precise as the sample is sequenced to a deeper level [[1](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-016-0881-8#ref-CR1 "Mortazavi A, Williams BA, McCue K, Schaeffer L, Wold B. Mapping and quantifying mammalian transcriptomes by RNA-Seq. Nat Methods. 2008;5:1–8.")]

> ### quality control
> FastQC [[11](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-016-0881-8#ref-CR11 "Andrews S. FASTQC. A quality control tool for high throughput sequence data. 
http://www.bioinformatics.babraham.ac.uk/projects/fastqc/
. Accessed 29 September 2014.")] is a popular tool to perform these analyses on Illumina reads, whereas NGSQC [[12](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-016-0881-8#ref-CR12 "Dai M, Thompson RC, Maher C, Contreras-Galindo R, Kaplan MH, Markovitz DM, et al. NGSQC: cross-platform quality analysis pipeline for deep sequencing data. BMC Genomics. 2010;11 Suppl 4:S7.")] can be applied to any platform.As a general rule, read quality decreases towards the 3’ end of reads, and if it becomes too low, bases should be removed to improve mappability. Software tools such as the FASTX-Toolkit [[13](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-016-0881-8#ref-CR13 "FASTX-Toolkit. 
http://hannonlab.cshl.edu/fastx_toolkit/
. Accessed 12 January 2016.")] and Trimmomatic [[14](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-016-0881-8#ref-CR14 "Bolger AM, Lohse M, Usadel B. Trimmomatic: a flexible trimmer for Illumina sequence data. Bioinformatics. 2014;30:2114–20.")] can be used to discard low-quality reads, trim adaptor sequences, and eliminate poor-quality bases.



