## Java Server Pages - EL and JSTL

As previously mentioned, scriptlets are largely outmoded. EL and JSTL can be used for many of the same functions.

This post will discuss:
* Expression Language
* JSTL

---

# Expression Language

Expression Language directly replaces expression tags. It is written in syntax:
>${func.}

EL supports the following types:
- Primitives
- Parameters, of defined Scope or otherwise
- Implicit objects in pageContext
- Methods within Scope

<br>

Most common functions, declarations, initializations, etc. cannot be executed within EL tags. EL should only be used to set/get data and execute methods that return data. Other logic should be executed within beans, then offloaded to the view component.

<br>

---

# Java Standard Tag Library
<br>

JSTL provides a set of HTML-like tags that provide Java Pages functionality within a JSP, without directly placing Java logic in a JSP document. The tags are as follows:

Output a value:
<pre><code class="language-xml">&lt;c:out value=&quot;BJ&quot;/&gt;
</code></pre>
<br>
Set a variable usable by JSTL tags within the document.
<pre><code class="language-xml">&lt;c:set var=&quot;OBJ&quot; value=&quot;OBJ&quot; scope=&quot;SCOPE&quot;/&gt;
</code></pre>
<br>
Remove a previously created variable.
<pre><code class="language-xml">&lt;c:remove var=&quot;OBJ&quot; scope=&quot;SCOPE&quot;/&gt;
</code></pre>
<br>
If statement. If the condition is true, code within the tags is parsed.
<pre><code class="language-xml">&lt;c:if test=&quot;CONDITION&quot; var=&quot;OBJ&quot;&gt;&lt;/c:if&gt;
</code></pre>
<br>
Switch case. If the condition for the case is true, code within the tags is parsed.
<pre><code class="language-xml">&lt;c:choose&gt;&lt;c:when test=&quot;CONDITION&quot;&gt;&lt;/c:when&gt;&lt;/c:choose&gt;
</code></pre>
<br>
For statement. If the condition is true, code within the tags is continuously parsed.
<pre><code class="language-html">//Standard FOR statement
&lt;c:forEach begin=&quot;INT&quot; end=&quot;INT&quot; step=&quot;INT&quot;&gt;&lt;c:forEach&gt;
//List/Enum FOR statement
&lt;c:forEach items=&quot;LIST&quot; var=&quot;OBJ&quot;&gt;&lt;c:forEach&gt;
</code></pre>
<br>
JSTL has the above core tags, but its functionality can be extended with other components of the JSTL library, such as *fn* functions.


**-gonkgonk**
