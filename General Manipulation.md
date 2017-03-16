**Stata Commands: describe, list, recast, compress, lable, summarize, codebook, inspect, tabulate format**
<pre><code></code></pre>
* Look over the data and variable: describe
* Set variable format: format
<pre><code>sysuse, auto, clear
describe
describe,detail
format price %6.2f
describe gear_ratio</code></pre>

* Look over the first several values of variable: list
* Change the variable type: recast
* Make the saving structure concise: compress
<pre><code>sysuse auto, clear
list gear_ratio in 1/20, sep(0)
recast int gear_ratio, force
compress</code></pre>

* Label data and variable: label
<pre><code>sysuse auto, clear
label data "This is a data about automobile"
label var foreign "0 domestic; 1 foreign"
des
</code></pre>
> label category variables like adding description about the numbers: label define & label values
<pre><code>browse
label define repair 1 "Good" 2 "Fairly Good" 3 "Not Good" 4"Almost Bad" 5"Bad"
label values rep78 repair
browse</code></pre>

* Basic stastics summary: summarize
<pre><code>sysuse auto, clear
summarize
summarize price
summarize price wei, detail
</code></pre>

* More statistics summary: codebook
> When the variable has values less than 9, stata will automatically treat it as category variable
<pre><code>codebook price weight
codebook rep78
</code></pre>

* More more statistics summary: inspect
<pre><code>inspect price weight</code></pre>

* Summarize the requency of category variable: tabulate
<pre><code>tabulate rep78</code></pre>

* Exchange the column and row: xpose
<pre><code>insheet using d51.txt, clear
xpose, clear</code></pre>
