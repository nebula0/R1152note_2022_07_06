extract exon fasta

python -m jcvi.formats.gff load GWHBDNU00000000.gff GWHBDNU00000000.genome.fa                                                                         sta --parents=mRNA --children=exon --id_attribute=ID -o GWHBDNU00000000.exon.fa                                                                         sta

python -m  jcvi.formats.fasta.some  