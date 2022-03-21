## Bootstrap Button Groups, Input Groups, Navbars, Pagination, Badges

The JS Bootstrap framework is a framework that provides tools for web design.

* Bootstrap Button Groups
* Bootstrap Input Groups
* Bootstrap Navbars
* Bootstrap Pagination
* Bootstrap Badges

<br>

---
# Bootstrap Button Groups
<br>
Buttons can be joined into one visual element in Bootstrap by inserting button elements into a *btn-group*.

<pre><code class="language-xml">    &lt;div class=&quot;btn-group&quot;&gt;
      &lt;button type=&quot;button&quot; class=&quot;btn btn-outline-primary&quot;&gt;Button 1 &lt;/button&gt;
      &lt;button type=&quot;button&quot; class=&quot;btn btn-outline-primary&quot;&gt;Button 2 &lt;/button&gt;
    &lt;/div&gt;
</code></pre>

Any type of button can be joined into a button group, for example, buttons attached to dropdown menus.

<br>
Yields the results:
<html lang="en">
  <body>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap + CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.10.2/dist/umd/popper.min.js" integrity="sha384-7+zCNj/IqJ95wo16oMtfsKbZ9ccEh31eOz1HGyDuCQ6wgnyJNSYdrPa03rtR1zdB" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.min.js" integrity="sha384-QJHtvGhmr9XOIpI6YVutG+2QOK9T+ZnN4kzFN1RtK3zEFEIsxhlmWl5/YESvpZ13" crossorigin="anonymous"></script>
<div class="container">
    <div class="btn-group-vertical">
      <button type="button" class="btn btn-outline-primary">Button 1 </button>
      <button type="button" class="btn btn-outline-primary">Button 2 </button>
      <div class="btn-group">
        <button type="button" data-bs-toggle="dropdown" class="btn btn-outline-primary dropdown-toggle"> Dropdown <span class="caret"> </span>
        </button>
        <ul class="dropdown-menu">
          <li><a class="dropdown-item" tabindex="-1" href="#">Menu 1</a></li>
          <li><a class="dropdown-item" tabindex="-1" href="#">Menu 2</a></li>
        </ul>
      </div>
    </div>
    </div>
  </body>
</html>

<br>

---
# Bootstrap Input Groups
<br>
Input forms/fields can have additional elements attached to the ends of the form. These can include text, buttons, etc.

<pre><code class="language-xml">    &lt;div class=&quot;input-group&quot;&gt;
        &lt;div class=&quot;input-group-prepend&quot;&gt;
      		&lt;span class=&quot;input-group-text&quot;&gt;Text&lt;/span&gt;
    	  &lt;/div&gt;
        &lt;input type=&quot;text&quot; class=&quot;form-control&quot; placeholder=&quot;Placeholder&quot;&gt;
        &lt;div class=&quot;input-group-append&quot;&gt;
          &lt;button type=&quot;button&quot; class=&quot;btn btn-primary dropdown-toggle&quot; data-bs-toggle=&quot;dropdown&quot;&gt; Dropdown  &lt;span class=&quot;caret&quot;&gt;&lt;/span&gt;
          &lt;/button&gt;
           &lt;ul class=&quot;dropdown-menu&quot; role=&quot;menu&quot;&gt;
             &lt;li&gt;&lt;a class=&quot;dropdown-item&quot; href=&quot;#&quot;&gt;Elements...&lt;/a&gt;&lt;/li&gt;
           &lt;/ul&gt;
    	  &lt;/div&gt;
    &lt;/div&gt;   
</code></pre>
<br>
Yields the result:
<br>
<html lang="en">
  <body>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap + CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.10.2/dist/umd/popper.min.js" integrity="sha384-7+zCNj/IqJ95wo16oMtfsKbZ9ccEh31eOz1HGyDuCQ6wgnyJNSYdrPa03rtR1zdB" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.min.js" integrity="sha384-QJHtvGhmr9XOIpI6YVutG+2QOK9T+ZnN4kzFN1RtK3zEFEIsxhlmWl5/YESvpZ13" crossorigin="anonymous"></script>
<div class="container">
    <div class="input-group">
    <div class="input-group-prepend">
      <span class="input-group-text">Text</span>
    </div>
    <input type="text" class="form-control" placeholder="Placeholder">
    <div class="input-group-append">
      <button type="button" class="btn btn-primary dropdown-toggle" data-bs-toggle="dropdown"> Dropdown  <span class="caret"></span>
      </button>
       <ul class="dropdown-menu" role="menu">
         <li><a class="dropdown-item" href="#">Elements...</a></li>
       </ul>
    </div>
    </div>
    </div>

  </body>
</html>
<br>

---
# Bootstrap Navbars
<br>
Bootstrap provides graphical elements for navbars and some limited dynamic functionality for them.

The syntax for a navbar is the following:
<pre><code class="language-xml">     <ul class="nav nav-tabs/pills">
         <li class="nav-item"><a class="nav-link" href="#">Elements...</a></li>
     </ul>  
</code></pre>
<br>
Navbars can be given some dynamic function by linking them to collapsing/fading/switching containers.

<pre><code class="language-xml">     &lt;h4&gt;Toggleable / Dynamic Pills&lt;/h4&gt;
  &lt;ul class=&quot;nav nav-pills&quot; role=&quot;tablist&quot;&gt;
    &lt;li class=&quot;nav-item&quot;&gt;
      &lt;a class=&quot;nav-link active&quot; data-bs-toggle=&quot;pill&quot; href=&quot;#home_p&quot;&gt;home&lt;/a&gt;
    &lt;/li&gt;
    &lt;li class=&quot;nav-item&quot;&gt;
      &lt;a class=&quot;nav-link&quot; data-bs-toggle=&quot;pill&quot; href=&quot;#menu1_p&quot;&gt;Menu 1&lt;/a&gt;
    &lt;/li&gt;
    &lt;li class=&quot;nav-item&quot;&gt;
      &lt;a class=&quot;nav-link&quot; data-bs-toggle=&quot;pill&quot; href=&quot;#menu2_p&quot;&gt;Menu 2&lt;/a&gt;
    &lt;/li&gt;
  &lt;/ul&gt;

  &lt;!-- Tab panes --&gt;
  &lt;div class=&quot;tab-content&quot;&gt;
    &lt;div id=&quot;home_p&quot; class=&quot;container tab-pane active&quot;&gt;&lt;br&gt;
      &lt;h3&gt;HOME&lt;/h3&gt;
      &lt;p&gt;Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.&lt;/p&gt;
    &lt;/div&gt;
    &lt;div id=&quot;menu1_p&quot; class=&quot;container tab-pane fade&quot;&gt;&lt;br&gt;
      &lt;h3&gt;Menu 1&lt;/h3&gt;
      &lt;p&gt;Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.&lt;/p&gt;
    &lt;/div&gt;
    &lt;div id=&quot;menu2_p&quot; class=&quot;container tab-pane fade&quot;&gt;&lt;br&gt;
      &lt;h3&gt;Menu 2&lt;/h3&gt;
      &lt;p&gt;Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam.&lt;/p&gt;
    &lt;/div&gt;
  &lt;/div&gt;
</code></pre>
<br>
Yields the result:
<br>
<html lang="en">
  <body>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap + CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.10.2/dist/umd/popper.min.js" integrity="sha384-7+zCNj/IqJ95wo16oMtfsKbZ9ccEh31eOz1HGyDuCQ6wgnyJNSYdrPa03rtR1zdB" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.min.js" integrity="sha384-QJHtvGhmr9XOIpI6YVutG+2QOK9T+ZnN4kzFN1RtK3zEFEIsxhlmWl5/YESvpZ13" crossorigin="anonymous"></script>
<div class="container">
    <h4>Toggleable / Dynamic Pills</h4>
  <ul class="nav nav-pills" role="tablist">
    <li class="nav-item">
      <a class="nav-link active" data-bs-toggle="pill" href="#home_p">home</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" data-bs-toggle="pill" href="#menu1_p">Menu 1</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" data-bs-toggle="pill" href="#menu2_p">Menu 2</a>
    </li>
  </ul>

  <!-- Tab panes -->
  <div class="tab-content">
    <div id="home_p" class="container tab-pane active"><br>
      <h3>HOME</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    </div>
    <div id="menu1_p" class="container tab-pane fade"><br>
      <h3>Menu 1</h3>
      <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
    </div>
    <div id="menu2_p" class="container tab-pane fade"><br>
      <h3>Menu 2</h3>
      <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam.</p>
    </div>
  </div>
  </div>

  </body>
</html>
<br>

---
# Bootstrap Pagination
<br>
Bootstrap provides a format for creating pagination elements. This attribute is applied to the list element, and attributes such as *active* or *disabled* can be applied for visual effect.

<pre><code class="language-xml">  &lt;ul class=&quot;pagination&quot;&gt;
    &lt;li class=&quot;page-item&quot;&gt;&lt;a class=&quot;page-link&quot; href=&quot;#&quot;&gt;«&lt;/a&gt;&lt;/li&gt;
    &lt;li class=&quot;page-item&quot;&gt;&lt;a class=&quot;page-link&quot; href=&quot;#&quot;&gt;1&lt;/a&gt;&lt;/li&gt;
    &lt;li class=&quot;page-item&quot;&gt;&lt;a class=&quot;page-link&quot; href=&quot;#&quot;&gt;2&lt;/a&gt;&lt;/li&gt;
    &lt;li class=&quot;page-item&quot;&gt;&lt;a class=&quot;page-link&quot; href=&quot;#&quot;&gt;3&lt;/a&gt;&lt;/li&gt;
    &lt;li class=&quot;page-item&quot;&gt;&lt;a class=&quot;page-link&quot; href=&quot;#&quot;&gt;4&lt;/a&gt;&lt;/li&gt;
    &lt;li class=&quot;page-item&quot;&gt;&lt;a class=&quot;page-link&quot; href=&quot;#&quot;&gt;»&lt;/a&gt;&lt;/li&gt;
   &lt;/ul&gt;
</code></pre>
<br>
Yields the result:
<br>
<html lang="en">
  <body>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap + CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.10.2/dist/umd/popper.min.js" integrity="sha384-7+zCNj/IqJ95wo16oMtfsKbZ9ccEh31eOz1HGyDuCQ6wgnyJNSYdrPa03rtR1zdB" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.min.js" integrity="sha384-QJHtvGhmr9XOIpI6YVutG+2QOK9T+ZnN4kzFN1RtK3zEFEIsxhlmWl5/YESvpZ13" crossorigin="anonymous"></script>

    <div class="container">
    <ul class="pagination">
        <li class="page-item disabled"><a class="page-link" href="#">«</a></li>
        <li class="page-item active"><a class="page-link" href="#">1</a></li>
        <li class="page-item"><a class="page-link" href="#">2</a></li>
        <li class="page-item"><a class="page-link" href="#">3</a></li>
        <li class="page-item"><a class="page-link" href="#">4</a></li>
        <li class="page-item"><a class="page-link" href="#">»</a></li>
       </ul>
       </div>

  </body>
</html>
<br>

---
# Bootstrap Badges
<br>
Bootstrap has visual elements in the form of badges, which are visual tags attached to interface elements.

<pre><code class="language-xml">   &lt;span class=&quot;badge bg-COLOR&quot;&gt;Badge&lt;/span&gt;
</code></pre>
<br>
Yields the result:
<br>
<html lang="en">
  <body>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap + CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.10.2/dist/umd/popper.min.js" integrity="sha384-7+zCNj/IqJ95wo16oMtfsKbZ9ccEh31eOz1HGyDuCQ6wgnyJNSYdrPa03rtR1zdB" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.min.js" integrity="sha384-QJHtvGhmr9XOIpI6YVutG+2QOK9T+ZnN4kzFN1RtK3zEFEIsxhlmWl5/YESvpZ13" crossorigin="anonymous"></script>
    <div class="container">
    <span class="badge bg-primary">Primary</span>
<span class="badge bg-secondary">Secondary</span>
<span class="badge bg-success">Success</span>
<span class="badge bg-danger">Danger</span>
<span class="badge bg-warning">Warning</span>
<span class="badge bg-info">Info</span>
<span class="badge bg-light">Light</span>
<span class="badge bg-dark">Dark</span>
    </div>

  </body>
</html>
<br>

-gonkgonk
