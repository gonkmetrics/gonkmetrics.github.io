## Introduction to Bootstrap Framework

The JS Bootstrap framework is a framework that provides tools for web design.

* Bootstrap Grid System

---
<br>
# Bootstrap Grid System

The Bootstrap grid system is an implementation of flexbox that can be used with simplified commands: !(display-flex).

The grid is divided into 12 column elements and supports any number of rows. The numbering of the column element determines it's position in the screen, although this depends on the size of inner elements as well.

The syntax for grid elements is shown below:
<pre><code class="language-xml">  &lt;div class=&quot;container&quot;&gt;
    &lt;div class=&quot;row&quot;&gt;
      &lt;div class=&quot;col-md-N&quot;&gt;CONTENT&lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
</code></pre>

Bootstrap parses the *class* attribute and applies only Bootstrap expressions, therefore other pure JS code (style, class names, etc.) can be written within the *class* attribute.

Possible Bootstrap expressions include the following:
<pre><code class="language-xml">&lt;div class=&quot;col-md-N text-ARGS p/m[x/y/t/b/l/r]-N border rounded-ARGS justify-ARGS align-ARGS&quot;&gt;CONTENT&lt;/div&gt;
</code></pre>

Note, this is the intersection between pure CSS and other frameworks: both allow you to apply visual rules to elements in a document, therefore the best one to use is whatever is easier/faster/more legible.

The 12 column element layout is strict, and it's width depends on the width of the container element.
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/bootstrap1.jpg" style="display: block; margin-left: auto; margin-right: auto; width: 50%;">

Therefore, if an individual column is made wider, it may take space from the remaining grid elements.

<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/bootstrap2.png" style="display: block; margin-left: auto; margin-right: auto; width: 50%;">

The left element is 3 wide, right is 8 wide, with a [offset-1] forming the whitespace.

The below document makes use of all the above concepts. CSS is written inline but should ideally be written in it's own block or imported as a stylesheet.
<pre><code class="language-xml">&lt;body&gt;
    &lt;div class=&quot;container&quot;&gt;
        &lt;div class=&quot;row&quot;&gt;
            &lt;div class=&quot;com-md-12 p-3&quot;&gt;
                &lt;h1 class=&quot;text-white rounded text-center p-3 title&quot; style=&quot;background-color: rgb(127, 197, 174);&quot;&gt;Lorem ipsum&lt;/h1&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        &lt;div class=&quot;row&quot;&gt;
            &lt;div class=&quot;col-md-2&quot;&gt;
                &lt;p class=&quot;text-white text-center border bg-secondary rounded px-2 py-4&quot;&gt;
                    Menu1&lt;br&gt;
                    Menu2&lt;br&gt;
                    Menu3&lt;br&gt;
                    Menu4
                &lt;/p&gt;
            &lt;/div&gt;
            &lt;div class=&quot;col-md-8&quot;&gt;
                Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Donec id augue sodales dui aliquam tempor.
                Nunc nec turpis vitae mauris viverra bibendum.
                Aenean convallis elit mattis, pulvinar est eget, sollicitudin velit.
                Nulla eget purus a augue blandit molestie a sit amet metus.
                Sed eu enim bibendum, ullamcorper risus et, lacinia nulla.
                Ut vel magna quis felis finibus ullamcorper.
                Aliquam sagittis ante eu egestas ultrices.
                Aenean luctus lacus a tortor suscipit mattis.
                &lt;br&gt;&lt;br&gt;
                &lt;span style=&quot;font-size: 2em&quot;&gt;...&lt;/span&gt;
            &lt;/div&gt;
            &lt;div class=&quot;col-md-2 justify-content-center align-items-center &quot;&gt;
                &lt;p class=&quot;rounded-pill py-3 text-center&quot; style=&quot;background-color: rgb(127, 197, 174);&quot;&gt;
                    Lorem
                    &lt;br&gt;ipsum.
                &lt;/p&gt;
                &lt;p class=&quot;rounded-pill py-3 text-center&quot; style=&quot;background-color: rgb(127, 197, 174);&quot;&gt;
                    Dolor
                    &lt;br&gt;sit amet.
                &lt;/p&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        &lt;hr&gt;
        &lt;div class=&quot;row&quot;&gt;
            &lt;div class=&quot;col-md-12&quot;&gt;
                &lt;p class=&quot;text-center footer&quot;&gt;Aenean luctus lacus a tortor suscipit mattis.&lt;/p&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/body&gt;
</code></pre>

Result:
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/bootstrap3.png" style="display: block; margin-left: auto; margin-right: auto; width: 50%;">

Having elements with padding OR margins is possible with 12 full column elements, given the size of the spacing is smaller than the potential overlaps. Additionally, marginY and paddingY, along with height are useful in limiting the height of column elements, as the default is fit-to-parent.


-gonkgonk
