# Stata code

## Getting started

1. Reading data

	use *sean.dta*
	summ zscore
	gen byte high=zscore>=1.5

2. More