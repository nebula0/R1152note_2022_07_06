#sequencing 

### GFF 
- General Feature Format
-  tab-delimited text file
-  CDs, microRNA, binding domain, ORFs...
-  many variation

#### GFF3
- most acceptable(this note created in 2022)
- 9 required field(some can be blank)
	1. sequence ID
	2. source
		- algorithm or procedure that generate this feature
	3. feature type
		- mRNA, domain...
		- [Sequence Ontology terms](http://www.sequenceontology.org/)
	4. feature start
	5. feature end
	6. score
		- E-value for similarity
		- P-value for prediction
	7. strand
	8. phase
		- where the feature begins with reference to the reading frame
		- 0, 1, or 2, indicating the number of bases that should be removed from the beginning of this feature to reach the first base of the next codon
	9. attributes
		- additional information 

![](https://learn.gencore.bio.nyu.edu/wp-content/uploads/2018/01/Screen-Shot-2018-01-07-at-10.08.12-PM-1024x368.png)
![](https://learn.gencore.bio.nyu.edu/wp-content/uploads/2018/01/Screen-Shot-2018-01-07-at-10.10.20-PM-1024x590.png)
[source](https://learn.gencore.bio.nyu.edu/ngs-file-formats/gff3-format/)

### fastq
- text-based format
- biological sequence (usually nucleotide sequence) and its corresponding quality scores
![](../attachment/Pasted%20image%2020220712164141.png)
![](../attachment/Pasted%20image%2020220712164203.png)
![](../attachment/Pasted%20image%2020220712164230.png)
![](../attachment/Pasted%20image%2020220712164241.png)
![](../attachment/Pasted%20image%2020220712164251.png)

### fasta
- text-based format
- nucleotide sequences or amino acid (protein) sequences
- line started with `>` was taken as a comment
sample
```
;LCBO - Prolactin precursor - Bovine
; a sample sequence in FASTA format
MDSKGSSQKGSRLLLLLVVSNLLLCQGVVSTPVCPNGPGNCQVSLRDLFDRAVMVSHYIHDLSS
EMFNEFDKRYAQGKGFITMALNSCHTSSLPTPEDKEQAQQTHHEVLMSLILGLLRSWNDPLYHL
VTEVRGMKGAPDAILSRAIEIEEENKRLLEGMEMIFGQVIPGAKETEPYPVWSGLPSLQTKDED
ARYSAFYNLLHCLRRDSSKIDTYLKLLNCRIIYNNNC*

>MCHU - Calmodulin - Human, rabbit, bovine, rat, and chicken
MADQLTEEQIAEFKEAFSLFDKDGDGTITTKELGTVMRSLGQNPTEAELQDMINEVDADGNGTID
FPEFLTMMARKMKDTDSEEEIREAFRVFDKDGNGYISAAELRHVMTNLGEKLTDEEVDEMIREA
DIDGDGQVNYEEFVQMMTAK*

>gi|5524211|gb|AAD44166.1| cytochrome b [Elephas maximus maximus]
LCLYTHIGRNIYYGSYLYSETWNTGIMLLLITMATAFMGYVLPWGQMSFWGATVITNLFSAIPYIGTNLV
EWIWGGFSVDKATLNRFFAFHFILPFTMVALAGVHLTFLHETGSNNPLGLTSDSDKIPFHPYYTIKDFLG
LLILILLLLLLALLSPDMLGDPDNHMPADPLNTPLHIKPEWYFLFAYAILRSVPNKLGGVLALFLSIVIL
GLMPFLHTSKHRSMMLRPLSQALFWTLTMDLLTLTWIGSQPVEYPYTIIGQMASILYFSIILAFLPIAGX
IENY
```

[source](https://en.wikipedia.org/wiki/FASTA_format)