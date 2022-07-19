download file from [current.geneontology.org/ontology/go.obo](http://current.geneontology.org/ontology/go.obo)
data-version: releases/2022-07-01

final file name `GO_term_name_type_all_cleaned_2022_07.tsv`

```bash
awk -v RS='Term' -v FS='\n' -v OFS='\t' 'NR>=4{print $2, $3, $4}' GO_term_to_name_full_2022_07.txt | grep id: | cut -f1 | cut -d " " -f2 > temp_go_term_all.txt


awk -v RS='Term' -v FS='\n' -v OFS='\t' 'NR>=4{print $2, $3, $4}' GO_term_to_name_full_2022_07.txt | grep id: | cut -f2 | cut -d " " -f1 --complement > temp_go_name_all.txt


awk -v RS='Term' -v FS='\n' -v OFS='\t' 'NR>=4{print $2, $3, $4}' GO_term_to_name_full_2022_07.txt | grep id: | cut -f3 | cut -d " " -f2 > temp_go_type_all.txt

paste temp_go_term_all.txt temp_go_name_all.txt | paste - temp_go_type_all.txt > GO_term_name_type_all_cleaned_2022_07.tsv

```