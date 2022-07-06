#R 


視套件是不是被下載了 回傳 bool
```R
"PACKAGE_NAME" %in% rownames(installed.packages()
```


回傳一些環境相關的參數?
```R
sessionInfo()
```


set working directory
```R
setwd("DIRECTORY")
```

取得現在的路徑
```R
getwd()
```


remove variables
```R
rm(list=ls()) # remove all vatiable
rm(list=lsf.str()) # remove all function but not variable
rm(list = setdiff(ls(), lsf.str())) # removes all objects except for functions
```

可以找套件說明書的東東 但不是所有套件都有
```R
browseVignettes("PACKAGE_NAME")
```

RStudio incompatible with R4.2.0. on Windows 10 (2022年5月20日)

老師 R 4.0.5
clusterprofiler 3.18.1