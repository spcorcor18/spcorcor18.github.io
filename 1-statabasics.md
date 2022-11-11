# 1 - Stata basics


### Interacting with Stata

* Submit commands via the Command window or menu bar (interactive mode), or through the do-file editor (batch mode).
* Review, Variables, Properties, and Results windows
* Paging up/down in the Command window to pull up recent commands
* Double-clicking commands in the Review window

###	Getting help: syntax

    help
    help keyword
    help regress
    help summarize
{: .lh-tight }

###	"Using Stata as a calculator"

	display 2 + 2
	display sqrt(49) + 10
{: .lh-tight }

Note: `sqrt` is one of Stata's many functions.

Abbreviations: Stata will accept abbreviated commands. You can use as few letters as you like, so long as the abbreviation remains unique to one command. If you use abbreviations, I recommend using at least as many letters that are needed for others reading your syntax to recognize the command.

<pre>
	<code>
 di 2 + 2
 dis <em>sqrt(49)</em> + 10
	</code>
</pre>

Common mathematical operators include +, -, \*, and /.  The exponent symbol is \^, for example: `di 7^2`. For longer expressions, use parentheses to make the intended order of operations clear. For example: `di (7+2)*4`. Type `help functions` to see a complete list of functions and operations.

The Expression Builder window is useful for constructing more complicated calculations that make use of operations, functions, saved results, and more. This is found under Data - Other Utilities - Hand Calculator - Create.

You may also use `display` for text expressions, for example:

    display "hello"

### Opening a data file in Stata format (.dta file)

```
use C:\data\myfilename.dta
use http://www.stata-press.com/data/r9/census2
```

Note that file names with spaces must be in quotes. I generally use quotation marks whether they are required or not.

    use “C:\data\my file name.dta”

The clear option tells Stata to remove any dataset already in memory and replace it with the specified one. Use this with caution, since unsaved changes will be lost. Most Stata commands have options that can be specified at the end of the line, following a comma:

	use C:\data\myfilename.dta, clear

Stata has some built-in datasets you can use to learn Stata. Type `help dta_examples` to see a list. You can open sample datasets directly using `sysuse`. A very common one is auto.dta:

	sysuse auto.dta