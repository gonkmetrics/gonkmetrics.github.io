## Bootstrap Buttons, Image Embeds, Dropdown Menus

The JS Bootstrap framework is a framework that provides tools for web design.

* Bootstrap Buttons
* Bootstrap Image Utils.
* Bootstrap Dropdown Menus

---
<br>
# Bootstrap Buttons

Bootstrap provides additional functionality to HTML buttons. These can be implemented in three ways:

<pre><code class="language-xml">    &lt;button type=&quot;button&quot; class=&quot;btn btn-ARGS:outline-ARGS:primary&quot;&gt;TEXT &lt;/button&gt;
    &lt;input type=&quot;button&quot; class=&quot;btn btn-ARGS:outline-ARGS:primary&quot; value=&quot;TEXT&quot;&gt;
    &lt;a href=&quot;#&quot; class=&quot;btn btn-ARGS:outline-ARGS:primary&quot; role=&quot;button&quot;&gt;TEXT &lt;/a&gt;
</code></pre>

<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/bootstrap4.png" style="display: block; margin-left: auto; margin-right: auto;">

Yields the results:
<pre><code class="language-html">//EMBED INTERACTIVE ELEMENT
</code></pre>

---
<br>
# Bootstrap Images

Bootstrap provides additional formatting options for images.

<pre><code class="language-xml">    &lt;img src=&quot;../images/image.jpg&quot; alt=&quot;NAME&quot; class=&quot;ARGS: rounded/img-fluid/img-thumbnail/float&quot;&gt;
</code></pre>

<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/bootstrap5.png" style="display: block; margin-left: auto; margin-right: auto;">

Yields the results:
<pre><code class="language-html">//EMBED INTERACTIVE ELEMENT
</code></pre>

---
<br>
# Bootstrap Dropdown Menus

Bootstrap can create interactive dropdown menus from list elements.

<pre><code class="language-xml">    &lt;div class=&quot;dropdown&quot;&gt;
      &lt;button class=&quot;btn btn-primary dropdown-toggle&quot; type=&quot;button&quot; data-bs-toggle=&quot;dropdown&quot;&gt;
        Button Title
      &lt;/button&gt;
      &lt;ul class=&quot;dropdown-menu&quot;&gt;
        &lt;li&gt;&lt;h6 class=&quot;dropdown-header&quot;&gt;Header 1&lt;/h6&gt;&lt;/li&gt;
        &lt;li&gt;&lt;hr class=&quot;dropdown-divider&quot;&gt;&lt;/li&gt;
        &lt;li&gt;&lt;a class=&quot;dropdown-item&quot; href=&quot;#&quot;&gt;Element 1&lt;/a&gt;&lt;/li&gt;
        &lt;li&gt;&lt;a class=&quot;dropdown-item disabled&quot; href=&quot;#&quot;&gt;Element 2 (Disabled)&lt;/a&gt;&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/div&gt;
</code></pre>

Yields the results:
<pre><code class="language-html">//EMBED INTERACTIVE ELEMENT
</code></pre>


-gonkgonk
