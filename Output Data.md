**Stata Commands: outfile, outsheet, xmlsave, dataout**

* Export .raw file: outfile
<pre><code> outfile using myauto, replace </code></pre>

* Export file with delimiter tab: outsheet
<pre><code> outsheet price wei len using myauto, replace </code></pre>

* Export .xml file: xmlsave
<pre><code> xmlsave auto, doctype(excel) replace </code></pre>

* Export word, Excel, Tex file: dataout
<pre><code>dataout, save(dataout01) excel replace
dataout, save(dataout02) word replace
dataout, save(dataout03) tex replace</code></pre>
