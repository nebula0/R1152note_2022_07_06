#R 

To understand the difference between class, I use the function `attributes()` to peek their attribute. Here they are.
```R
> attributes(fc_condition)
$levels
[1] "up"    "basal"

$class
[1] "factor"

> attributes(list_collapse)
$names
[1] "datETcollapsed" "group2row"      "selectedRow" 
```