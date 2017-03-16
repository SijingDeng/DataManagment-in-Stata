* Stata Commands: infile, insheet, infix, use, xmluse

* Data with delimiter "tab": insheet
<pre><code>type d11.txt
insheet v1 v2 v3 using d11.txt, clear </code></pre>

* Data with delimiter "blank": infile
<pre><code> insheet using d21.txt, clear delimiter(" ") </code></pre>
> need to claim the type of delimiter when using 'insheet'
<pre><code> infile v1 v2 v3 using d21.txt, clear </code></pre>

* Data with delimiter "comma": infile
<pre><code> infile v1 v2 v3 using d3.txt, clear</code></pre>
   
* Data with string: infile
> Need to claim the type of data when importing otherwise those values will be replaced with NaN
<pre><code> infile str30 v1 int v2 str10 v3 using d3.txt, clear </code></pre>

* Stata data: use
<pre><code> use d3.dta, clear </code></pre>

* Excel data: xmluse
> we need to save file.xls as file.xml first
<pre><code> xmluse dl.xml, doctype(excel) clear first row
compress </code></pre>
> make the saving structure compress

