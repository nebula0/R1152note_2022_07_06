#work_note 

2022_07_17
Because copy GWHAAEX00000000_annotation.txt from the website did not includ all rows(I should right-click and download the file rather than copy texts )
the processes were redone again and made some adjustments. 


## gmap

pre-requird step, build some files that will be use later
`gmap_build -D Gastrodia_elata_gmap_build -d GWHBDNU_2021 ./GWHBDNU00000000.genome.fasta`


map GWHAAEX00000000.RNA.fasta to GWHBDNU00000000.genome.fasta
`gmap -B 4 -t 30 --nofails -f 2 -D ~/genome.fasta/Gastrodia/Gastrodia_elata_gmap_build/GWHBDNU_2021/ -d GWHBDNU_2021 ./GWHAAEX00000000.RNA.fasta > GWHAAEX00000000-RNA.gmap-format2-GWHBDNU-genome.gff3
`
variable details are in `gmap --help`


---

#### chromosome name in GWHBDNU00000000.genome.fasta example
`GWHBDNU00000001`

```
$ cat GWHBDNU00000000.genome.fasta | grep GWH
>GWHBDNU00000001        Chromosome 1    Complete=T      Circular=F      OriSeqID=Chr1   Len=132907784
>GWHBDNU00000002        Chromosome 2    Complete=T      Circular=F      OriSeqID=Chr2   Len=107263584
>GWHBDNU00000003        Chromosome 3    Complete=T      Circular=F      OriSeqID=Chr3   Len=72887854
>GWHBDNU00000004        Chromosome 4    Complete=T      Circular=F      OriSeqID=Chr4   Len=70721811
>GWHBDNU00000005        Chromosome 5    Complete=T      Circular=F      OriSeqID=Chr5   Len=62286500
>GWHBDNU00000006        Chromosome 6    Complete=T      Circular=F      OriSeqID=Chr6   Len=51980826
>GWHBDNU00000007        Chromosome 7    Complete=T      Circular=F      OriSeqID=Chr7   Len=51759935
>GWHBDNU00000008        Chromosome 8    Complete=T      Circular=F      OriSeqID=Chr8   Len=51280010
>GWHBDNU00000009        Chromosome 9    Complete=T      Circular=F      OriSeqID=Chr9   Len=50097291
>GWHBDNU00000010        Chromosome 10   Complete=T      Circular=F      OriSeqID=Chr10  Len=50090255
>GWHBDNU00000011        Chromosome 11   Complete=T      Circular=F      OriSeqID=Chr11  Len=48917039
>GWHBDNU00000012        Chromosome 12   Complete=T      Circular=F      OriSeqID=Chr12  Len=43897423
>GWHBDNU00000013        Chromosome 13   Complete=T      Circular=F      OriSeqID=Chr13  Len=43286343
>GWHBDNU00000014        Chromosome 14   Complete=T      Circular=F      OriSeqID=Chr14  Len=42029776
>GWHBDNU00000015        Chromosome 15   Complete=T      Circular=F      OriSeqID=Chr15  Len=40924768
>GWHBDNU00000016        Chromosome 16   Complete=T      Circular=F      OriSeqID=Chr16  Len=36350181
>GWHBDNU00000017        Chromosome 17   Complete=T      Circular=F      OriSeqID=Chr17  Len=35279129
>GWHBDNU00000018        Chromosome 18   Complete=T      Circular=F      OriSeqID=Chr18  Len=33956578
>GWHBDNU00000019        OriSeqID=Chr0   Len=9450064
>GWHBDNU00000020        Chloroplast     Complete=T      Circular=T      OriSeqID=ChrC   Len=35304
>GWHBDNU00000021        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM1  Len=31165
>GWHBDNU00000022        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM2  Len=23418
>GWHBDNU00000023        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM3  Len=85046
>GWHBDNU00000024        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM4  Len=74858
>GWHBDNU00000025        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM5  Len=101157
>GWHBDNU00000026        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM6  Len=110758
>GWHBDNU00000027        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM7  Len=410335
>GWHBDNU00000028        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM8  Len=59170
>GWHBDNU00000029        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM9  Len=24896
>GWHBDNU00000030        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM10 Len=51430
>GWHBDNU00000031        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM11 Len=34182
>GWHBDNU00000032        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM12 Len=25189
>GWHBDNU00000033        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM13 Len=13502
>GWHBDNU00000034        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM14 Len=20368
>GWHBDNU00000035        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM15 Len=34107
>GWHBDNU00000036        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM16 Len=18026
>GWHBDNU00000037        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM17 Len=120640
>GWHBDNU00000038        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM18 Len=34580
>GWHBDNU00000039        Mitochondrion   Complete=F      Circular=F      OriSeqID=ChrM19 Len=66997

```

#### sequence ID(column 1) in GWHBDNU00000000.gff example
`GWHBDNU00000019` -> same as GWHBDNU00000000.genome.fasta chromosome id

```
$ head GWHBDNU00000000.gff
##gff-version 3
#OriSeqID=Chr0  Accession=GWHBDNU00000019
GWHBDNU00000019 GelGenome       gene    446429  446845  .       +       .       ID=GelC19G00001;Accession=GWHGBDNU000001;Name=GelC19G00001;old_id=evm.TU.Chr0.2;transl_table=1
GWHBDNU00000019 GelGenome       mRNA    446429  446845  .       +       .       ID=GelC19G00001.1;Accession=GWHTBDNU000001;Name=GelC19G00001.1;Parent=GelC19G00001;Parent_Accession=GWHGBDNU000001;old_id=evm.model.Chr0.2;transl_table=1
GWHBDNU00000019 GelGenome       exon    446429  446435  .       +       .       ID=GelC19G00001.1.exon.1;Name=GelC19G00001.1.exon.1;Parent=GelC19G00001.1;Parent_Accession=GWHTBDNU000001;old_id=evm.model.Chr0.2.exon1;transl_table=1
GWHBDNU00000019 GelGenome       CDS     446429  446435  .       +       0       ID=GelC19G00001.1.cds.1;Name=GelC19G00001.1.cds.1;Parent=GelC19G00001.1;Parent_Accession=GWHTBDNU000001;Protein_Accession=GWHPBDNU000001;old_id=cds.evm.model.Chr0.2;transl_table=1
GWHBDNU00000019 GelGenome       exon    446457  446845  .       +       .       ID=GelC19G00001.1.exon.2;Name=GelC19G00001.1.exon.2;Parent=GelC19G00001.1;Parent_Accession=GWHTBDNU000001;old_id=evm.model.Chr0.2.exon2;transl_table=1
GWHBDNU00000019 GelGenome       CDS     446457  446845  .       +       1       ID=GelC19G00001.1.cds.2;Name=GelC19G00001.1.cds.2;Parent=GelC19G00001.1;Parent_Accession=GWHTBDNU000001;Protein_Accession=GWHPBDNU000001;old_id=cds.evm.model.Chr0.2;transl_table=1
GWHBDNU00000019 GelGenome       gene    552367  552927  .       -       .       ID=GelC19G00002;Accession=GWHGBDNU000002;Name=GelC19G00002;old_id=evm.TU.Chr0.3;transl_table=1
```


#### sequence ID(column 1) in GWHAAEX00000000-RNA.gmap-format2-GWHBDNU-genome.gff3 example
`GWHBDNU00000019` -> same as GWHBDNU00000000.genome.fasta chromosome id
additional information (column 9) different from [sequence ID column 1 in GWHBDNU00000000 gff example](#sequence%20ID%20column%201%20in%20GWHBDNU00000000%20gff%20example)
because mRNA are from GWHAAEX00000000.RNA.fasta
```
$ head  GWHAAEX00000000-RNA.gmap-format2-GWHBDNU-genome.gff3
##gff-version   3
# Generated by GMAP version 2021-12-17 using call:  gmap.avx2 -B 4 -t 30 --nofails -f 2 -D /home/hpc/ls7046-5/genome.fasta/Gastrodia/Gastrodia_elata_gmap_build/GWHBDNU_2021/ -d GWHBDNU_2021 ./GWHAAEX00000000.RNA.fasta
GWHBDNU00000013 GWHBDNU_2021    gene    21319753        21319950        .       +       .       ID=GWHTAAEX000014.path1;Name=GWHTAAEX000014;Dir=indeterminate
GWHBDNU00000013 GWHBDNU_2021    mRNA    21319753        21319950        .       +       .       ID=GWHTAAEX000014.mrna1;Name=GWHTAAEX000014;Parent=GWHTAAEX000014.path1;Dir=indeterminate;coverage=100.0;identity=99.5;matches=197;mismatches=1;indels=0;unknowns=0
GWHBDNU00000013 GWHBDNU_2021    exon    21319753        21319950        99      +       .       ID=GWHTAAEX000014.mrna1.exon1;Name=GWHTAAEX000014;Parent=GWHTAAEX000014.mrna1;Target=GWHTAAEX000014 198 1 .
GWHBDNU00000013 GWHBDNU_2021    CDS     21319753        21319950        99      +       0       ID=GWHTAAEX000014.mrna1.cds1;Name=GWHTAAEX000014;Parent=GWHTAAEX000014.mrna1;Target=GWHTAAEX000014 198 1 .
###
GWHBDNU00000013 GWHBDNU_2021    gene    23181047        23182523        .       -       .       ID=GWHTAAEX000020.path1;Name=GWHTAAEX000020;Dir=indeterminate
GWHBDNU00000013 GWHBDNU_2021    mRNA    23181047        23182523        .       -       .       ID=GWHTAAEX000020.mrna1;Name=GWHTAAEX000020;Parent=GWHTAAEX000020.path1;Dir=indeterminate;coverage=100.0;identity=99.9;matches=1476;mismatches=1;indels=0;unknowns=0
GWHBDNU00000013 GWHBDNU_2021    exon    23181047        23182523        99      -       .       ID=GWHTAAEX000020.mrna1.exon1;Name=GWHTAAEX000020;Parent=GWHTAAEX000020.mrna1;Target=GWHTAAEX000020 1477 1 .
```

## gffcompare
the previous step only map GWHAAEX00000000.RNA.fasta to GWHBDNU00000000.genome.fasta, but we still didn't get ID-ID relation.

```
gffcompare -r GWHBDNU00000000.gff GWHAAEX00000000-RNA.gmap-format2-GWHBDNU-genome.gff3
```

output files, maybe create a folder to place them will be better 
```
gffcmp.annotated.gtf
gffcmp.GWHAAEX00000000-RNA.gmap-format2-GWHBDNU-genome.gff3.refmap
gffcmp.GWHAAEX00000000-RNA.gmap-format2-GWHBDNU-genome.gff3.tmap 
gffcmp.loci 
gffcmp.stats 
gffcmp.tracking   
```

### other process
```bash
# generate two column file
cut -f1,4 gffcmp.GWHAAEX00000000-RNA.gmap-format2-GWHBDNU-genome.gff3.tmap | cut -f1 -d '.' | sed 1d | sed -e's/GWHTAAEX/GWHGAAEX/g'|sort -k1nr > IDtwo_column_pre.tsv

# delete line if first filed == "-"
awk '$1 != "-"{print $0}' IDtwo_column_pre.tsv > IDtwo_column_pre_no-.tsv

# group element based on second field(GWHAAEX00000000 gene ID index)
python -m jcvi.formats.base group --groupby=1 IDtwo_column_pre_no-.tsv > IDtwo_column_sort_by_GWHA.tsv

# replace gene ID from GWHAAEX00000000 to GWHBDNU00000000
awk -v OFS="\t" -v FS="\t" 'FNR==NR {a[$2]=$1; next} $1 in a {print a[$1], $2, $3, $4, $5}' IDtwo_column_sort_by_GWHA.tsv GWHAAEX00000000_annotation.txt > temp_GWHBDNU00000000_annotation.txt 

# 
perl -lane 'chomp; @l = split /\t/; for $c1(split /,/, $l[0]) { print join "\t", $c1, $l[1]; }' temp_GWHBDNU00000000_annotation.txt  > temp_ID_c1.tsv

perl -lane 'chomp; @l = split /\t/; for $c1(split /,/, $l[0]) { print join "\t", $c1, $l[2]; }' temp_GWHBDNU00000000_annotation.txt > temp_ID_c2.tsv

perl -lane 'chomp; @l = split /\t/; for $c1(split /,/, $l[0]) { print join "\t", $c1, $l[3]; }' temp_GWHBDNU00000000_annotation.txt > temp_ID_c3.tsv

perl -lane 'chomp; @l = split /\t/; for $c1(split /,/, $l[0]) { print join "\t", $c1, $l[4]; }' temp_GWHBDNU00000000_annotation.txt > temp_ID_c4.tsv

# split 1st column then join with 2nd column

# a,b,c 1 -> a 1
# ?? ?? ?? ?? ?? ??b 1??
# ?? ?? ?? ?? ?? ??c 1??

join temp_ID_c1.tsv temp_ID_c2.tsv | join - temp_ID_c3.tsv | join - temp_ID_c4.tsv > GWHBDNU00000000_annotation.txt
 ```
script explanation:[22_05_2022?????? awk join](22_05_2022??????%20awk%20join.md)




%%---

???????????????????????????? ????????????
```
$ head Gelata.GOterm-to-GDNUgene.tsv
GO:0005975      GelC13G00541
GO:0004650      GelC13G00541
GO:0005515      GelC13G00544
GO:0003676      GelC13G00552
GO:0008270      GelC13G00552
GO:0009055      GelC13G00553
GO:0016787      GelC13G00554
GO:0070006      GelC13G00554
GO:0016021      GelC13G00557
GO:0016192      GelC13G00557

```%%

