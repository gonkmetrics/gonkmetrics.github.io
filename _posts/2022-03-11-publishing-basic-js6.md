## Basic Javascript 6

Today's I used the JS library jQuery. This library extends the functionality of JS by simplifying DOM selections for HTML documents, along other features.

The first step in using jQuery is to import it into a document. The easiest way to do this is to add the below referrer:
<pre><code class="language-javascript"><script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
</code></pre>

This enables jQuery functionality in a document. Note that the script should be written in a separate &lt;script&gt; block for jQuery to work.

* Basic jQuery Syntax
* Basic jQuery Selectors

---
<br>
# Basic jQuery Syntax:

All jQuery commands start with:
<pre><code class="language-javascript">$("element").function;
</code></pre>

Additionally functions can be defined within jQuery commands:
<pre><code class="language-javascript">$(function(){code...}
</code></pre>

Commands support multiple methods for querying:
> jQuery methods such as .parent(), children(), .next/prev(), .siblings(). Additionally, leading colon :element to select all nodes.

> Or regular JS syntax: parent>child, upper lower, #id, .class, $(opposite).

The below commands selects the child element 'CHILD_OF_OBJECT_A' from 'OBJECT_A':
<pre><code class="language-javascript">$("OBJECT_A").children("CHILD_OF_OBJECT_A").function);
</code></pre>

There is also a .css function that appends CSS commands to the selected objects.
<pre><code class="language-javascript">$("OBJECT_A").css("font-size","20px").css("background-color","yellow");
</code></pre>

.nextElementSibling has it's equivalent in jQuery:
<pre><code class="language-javascript">$("OBJECT_A").next().function;
</code></pre>

Along with targeted sibling selections:
<pre><code class="language-javascript">$("OBJECT_A").siblings("li");
</code></pre>

Finally, jQuery commands can be used to select and assign an object to a variable:
<pre><code class="language-javascript">var cobj6 = $(".obj6");
</code></pre>

---
<br>
# jQuery Selectors:

Expands on DOM selections by adding selection functionality:

Selector for odd-numbered objects:
<pre><code class="language-javascript">$("object:odd")
</code></pre>

Selector for even-numbered objects:
<pre><code class="language-javascript">$("object:even")
</code></pre>

Selector for firstt object(of multiple):
<pre><code class="language-javascript">$("object:first")
</code></pre>

Selector for last object(of multiple):
<pre><code class="language-javascript">$("object:last")
</code></pre>

Selector for object at index N:
<pre><code class="language-javascript">$("object:eq(N)")
</code></pre>

Selector for objects less than index N:
<pre><code class="language-javascript">$("object:lt(N)")
</code></pre>

Selector for objects greater than index N:
<pre><code class="language-javascript">$("object:gt(N)")
</code></pre>


-gonkgonk
