#work_note

I used the sequence in Li-Hsuan Ho(2020)[^1] supplement data, which are primer, to blast genome sequence in Yuxing Xu(2021)[^2]

the sequence which I used
```
# primer in Li-Hsuan Ho(2020)
>GeSUT4-5-BP
GGGGACAAGTTTGTACAAAAAAGCAGGCTATGGCAGATCCACCGCTTCAGTTGGC
>GeSUT4D-3-BP
GGGGACCACTTTGTACAAGAAAGCTGGGTT TTA CTCAACTGCCAAAGGAACCCCA
>GeSUT4-3-BP
GGGGACCACTTTGTACAAGAAAGCTGGGTATTC ATCTTCGGTCCTTCTGCTTTGC
>GeSUT3-5-BP
GGGGACAAGTTTGTACAAAAAAGCAGGCTGAAT GAG ATCTACCGAGCGAGGCCG
>GeSUT3-3-BP
GGGGACCACTTTGTACAAGAAAGCTGGGTGATC AGTGCATGCTGCCCATAGTTGC

# genome sequence in Yuxing Xu(2021)
too long, so i past directory here:
## CDs
/scratch/ls7046/ls7046-5/genome.fasta/Gastrodia/sucrose_exon_mRNA.txt

## mRNA
/scratch/ls7046/ls7046-5/genome.fasta/Gastrodia/sucrose_mRNA.txt
```

result
```
# CDs

Query: GeSUT4-5-BP Query ID: lcl|Query_42202 Length: 55


>GelC07G01120.1
Sequence ID: Query_42214 Length: 2365
Range 1: 264 to 289

Score:48.2 bits(52), Expect:2e-09, 
Identities:26/26(100%),  Gaps:0/26(0%), Strand: Plus/Plus

Query  30   ATGGCAGATCCACCGCTTCAGTTGGC  55
            ||||||||||||||||||||||||||
Sbjct  264  ATGGCAGATCCACCGCTTCAGTTGGC  289
```

```
# mRNA

Query: GeSUT4-5-BP Query ID: lcl|Query_28084 Length: 55


>GelC07G01120
Sequence ID: Query_28096 Length: 219041
Range 1: 264 to 289

Score:48.2 bits(52), Expect:3e-08, 
Identities:26/26(100%),  Gaps:0/26(0%), Strand: Plus/Plus

Query  30   ATGGCAGATCCACCGCTTCAGTTGGC  55
            ||||||||||||||||||||||||||
Sbjct  264  ATGGCAGATCCACCGCTTCAGTTGGC  289




Range 2: 26574 to 26599

Score:48.2 bits(52), Expect:3e-08, 
Identities:26/26(100%),  Gaps:0/26(0%), Strand: Plus/Plus

Query  30     ATGGCAGATCCACCGCTTCAGTTGGC  55
              ||||||||||||||||||||||||||
Sbjct  26574  ATGGCAGATCCACCGCTTCAGTTGGC  26599




Range 3: 54107 to 54132

Score:48.2 bits(52), Expect:3e-08, 
Identities:26/26(100%),  Gaps:0/26(0%), Strand: Plus/Plus

Query  30     ATGGCAGATCCACCGCTTCAGTTGGC  55
              ||||||||||||||||||||||||||
Sbjct  54107  ATGGCAGATCCACCGCTTCAGTTGGC  54132




Range 4: 81640 to 81665

Score:48.2 bits(52), Expect:3e-08, 
Identities:26/26(100%),  Gaps:0/26(0%), Strand: Plus/Plus

Query  30     ATGGCAGATCCACCGCTTCAGTTGGC  55
              ||||||||||||||||||||||||||
Sbjct  81640  ATGGCAGATCCACCGCTTCAGTTGGC  81665




Range 5: 109173 to 109198

Score:48.2 bits(52), Expect:3e-08, 
Identities:26/26(100%),  Gaps:0/26(0%), Strand: Plus/Plus

Query  30      ATGGCAGATCCACCGCTTCAGTTGGC  55
               ||||||||||||||||||||||||||
Sbjct  109173  ATGGCAGATCCACCGCTTCAGTTGGC  109198




Range 6: 136706 to 136731

Score:48.2 bits(52), Expect:3e-08, 
Identities:26/26(100%),  Gaps:0/26(0%), Strand: Plus/Plus

Query  30      ATGGCAGATCCACCGCTTCAGTTGGC  55
               ||||||||||||||||||||||||||
Sbjct  136706  ATGGCAGATCCACCGCTTCAGTTGGC  136731




Range 7: 164239 to 164264

Score:48.2 bits(52), Expect:3e-08, 
Identities:26/26(100%),  Gaps:0/26(0%), Strand: Plus/Plus

Query  30      ATGGCAGATCCACCGCTTCAGTTGGC  55
               ||||||||||||||||||||||||||
Sbjct  164239  ATGGCAGATCCACCGCTTCAGTTGGC  164264




Range 8: 191772 to 191797

Score:48.2 bits(52), Expect:3e-08, 
Identities:26/26(100%),  Gaps:0/26(0%), Strand: Plus/Plus

Query  30      ATGGCAGATCCACCGCTTCAGTTGGC  55
               ||||||||||||||||||||||||||
Sbjct  191772  ATGGCAGATCCACCGCTTCAGTTGGC  191797
```

[^1]:GeSUT4 mediates sucrose import at the symbiotic interface for carbon allocation of heterotrophic Gastrodia elata(Orchidaceae)
[^2]:A chromosome-scale Gastrodia elata genome and large-scale comparative genomic analysis indicate convergent evolution by gene loss in mycoheterotrophic and parasitic plants