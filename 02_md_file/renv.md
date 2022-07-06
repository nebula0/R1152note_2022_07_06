#R 

```R
renv::snapshot()
```
If you call `renv::snapshot()`, the lockfile will be updated, with the version of R that you're currently using for the project
這樣看來她它不會自動在更動套件或R版本後更新 renv.lock，變成要記得手動弄?