# Stata code

[Custom foo description](#getting-started)

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