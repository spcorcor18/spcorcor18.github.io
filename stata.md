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


```
{
	use *sean.dta*
	summ zscore
	gen byte high=zscore>=1.5
}
```

### More 1

### More 2