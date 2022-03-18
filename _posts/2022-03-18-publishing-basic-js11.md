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
{% include A1_button.html %}

---
<br>
# Bootstrap Images

Bootstrap provides additional formatting options for images.

<pre><code class="language-xml">    &lt;img src=&quot;../images/image.jpg&quot; alt=&quot;NAME&quot; class=&quot;ARGS: rounded/img-fluid/img-thumbnail/float&quot;&gt;
</code></pre>

In the below image, a mock profile page was made, with the profile picture being an image inside a bootstrap grid element with *class="rounded"* applied.

<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/bootstrap5.png" style="display: block; margin-left: auto; margin-right: auto;">

---
<br>
# Bootstrap Dropdown Menus

Bootstrap can create interactive dropdown menus from list elements. Multiple arguments exist for structuring the dropdown menu.

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
{% include A1_dropdown.html %}

<html lang="en">
  <body>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.10.2/dist/umd/popper.min.js" integrity="sha384-7+zCNj/IqJ95wo16oMtfsKbZ9ccEh31eOz1HGyDuCQ6wgnyJNSYdrPa03rtR1zdB" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.min.js" integrity="sha384-QJHtvGhmr9XOIpI6YVutG+2QOK9T+ZnN4kzFN1RtK3zEFEIsxhlmWl5/YESvpZ13" crossorigin="anonymous"></script>

    <div class="dropdown">
      <button class="btn btn-primary dropdown-toggle" type="button" data-bs-toggle="dropdown">
        Button Title
      </button>
      <ul class="dropdown-menu">
        <li><h6 class="dropdown-header">Header 1</h6></li>
        <li><hr class="dropdown-divider"></li>
        <li><a class="dropdown-item" href="#">Element 1</a></li>
        <li><a class="dropdown-item disabled" href="#">Element 2 (Disabled)</a></li>
      </ul>
    </div>


  </body>
</html>


-gonkgonk
