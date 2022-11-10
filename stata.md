# Stata code

[Custom foo description](#more-2)

## Getting started

### Reading data

```
use *sean.dta*
summ zscore
gen byte high=zscore>=1.5
```

### More

1. Code block one

        gen sean=1
        replace sean=2 if sean==1

2. Code block two

        egen sean2=max(score),by(group)
        duplicates report sean2


### More 1

### More 2