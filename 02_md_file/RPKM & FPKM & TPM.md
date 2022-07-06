#sequence_processing 

## RPKM & FPKM
## RPKM, reads per kilobase million
Reads per kilobase of exon model per million reads [ref](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-016-0881-8)

- first normalize `read` then `length` 
- for single end
1. `per million scaling factor`:  $\cfrac{total\ reads \ number}{1,000,000}$
2. `RPM` = $\cfrac{read\ counts}{per million scaling factor}$
3. `per kilo scaling factor`:$\cfrac{length\ of\ gene}{1000}$
4. `RPKM` = $\cfrac{RPM}{perkilo scaling}$

## FPKM, fragment per kilobase million
- first normalize `read` then `length`, same as RPKM
- for paired end, two reads correspond to same fragment will be count once, if only one read in the pair mapped, it will also be count once.
## TPM, Transcripts Per Kilobase Million (k呢???)
- similar to above two, but normalization order is different.
1. `per kilo scaling factor`:$\cfrac{length\ of\ gene}{1000}$
2. `RPK` = $\cfrac{read\ counts}{per kilo\ scaling\ factor}$
3. `per million scaling factor`:  $\cfrac{total\ reads \ number}{1,000,000}$
4. `TPM` = $cfrac{RPK}{per million scaling factor}$

because TPM do normalization for total read count  in the later step, this will let different sample have same total scaled read count, thus sometimes more easy to compare.

> why no TPM for paired end ?

ref
https://www.rna-seqblog.com/rpkm-fpkm-and-tpm-clearly-explained/