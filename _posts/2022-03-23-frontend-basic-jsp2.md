## Jakarta Server Pages - Expression Tag, Directive Tag, Inline Comments

Jakarta (form. Java) Server Pages is a framework used for web application development.

This post will discuss:
* Expression Tag
* Directive Tag
* Inline Comment Types

<br>

---
# Expression Tag
<br>

**&lt;%= %&gt;**
Expression tags allow JSP code to be output directly into the document code stream. Therefore, any output from JSP does not need to be explicitly printed.

<pre><code class="language-xml">&lt;%
out.println(&quot;name:&quot;+name+&quot;&lt;br&gt;&quot;);
out.println(&quot;age:&quot;+age+&quot;&lt;br&gt;&quot;);
out.println(&quot;area:&quot;+areaCircle(5));
%&gt;
&lt;br&gt; *SAME AS*
name:&lt;%= name %&gt;&lt;br&gt;
age:&lt;%= age %&gt;&lt;br&gt;
area: &lt;%= areaCircle(5) %&gt;
</code></pre>
<br>

---
# Directive Tag
<br>

**&lt;%@ %&gt;**
The Directive Tag contains commands for running the JSP page in the servlet.

>Language:
>>Defines scripting language. Default is "java"

>contentType:
>>Defines MIME, character set.

>pageEncoding:
>>Encoding. Set to UTF-8 for international language support.


---
# Inline Comment Types
<br>

Since Java and HTML are being used simultaneously, all forms of comment tags are available for use:
<ul>
<li>//</li>
<li>/* */</li>
<li>&lt;!-- --&gt;</li>
<li>&lt;%-- --%&gt;</li>
</ul>

<br>
As the functionality of JSP suggests, Java comments are not exposed to the client browser, while HTML comments can be read by the client browser. (i.e. seen through *inspect element*)

<br>

-gonkgonk
