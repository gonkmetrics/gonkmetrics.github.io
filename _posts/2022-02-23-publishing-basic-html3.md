## Basic HTML 3

<head>
  <meta charset="utf-8">
  <title>highlight.js demo</title>
	<link rel="alternate stylesheet" title="A 11 Y Light" href="styles/a11y-light.css" disabled="disabled">
</head>

For this session basic HTML was reviewed together with the beginnings of CSS.

Three distinct concepts were covered:

* Additional HTML form tags
* Groupings in HTML
* Basic CSS

---

Additional Form Tags:
Lists have syntax <li> and are ordered in DOWNARDS order. Lists can be nested into each other and different kinds of lists can be used within each other.

<pre><code class="language-html">
<!DOCTYPE html>
<html>
<head>
    <style>
        * { margin : 10px }
    </style>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>formoption3</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <link rel='stylesheet' type='text/css' media='screen' href='main.css'>
    <script src='main.js'></script>
</head>
<body>
    disabled:
    <fieldset>
        <legend>writing here:</legend><form>
            <p>write: <input type="text" value="abcd" readonly/></p>
            <p>title: <input type="text"/></p>
            <textarea cols="30" rows="10"></textarea>
            <input type="submit" value="ubit"/>
            <input type="reset" value="reset"/>
        </form>
    </fieldset>
</body>
</html>
</code></pre>

---

Groupings:
<pre><code class="language-html">
<!DOCTYPE html>
<html>
<head>
    <style>
        body > div {
            border: 1px solid black;
        }
    </style>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>layoutprac</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <link rel='stylesheet' type='text/css' media='screen' href='main.css'>
    <script src='main.js'></script>
</head>
<body>
    <div id="header">
        <h1>topdev Company</h1>
        <br>
        <ul>
            <li><a href="#">회사 안내</a></li>
            <li><a href="#">제푼 소개</a></li>
            <li><a href="#">강의 문의</a></li>
            <li><a href="#">연락</a></li>
        </ul>
    </div>
    <div id="maincontainer">
        <div id="leftcontainer">
            <p>Content 1</p>
        </div>
        <div id="centercontainer">
            <p>Content 2</p>
        </div>
        <div id="rightcontainer">
            <p>Content 3</p>
            </div>
    </div>
    <div id="footer">
        <address>주소는 곧 준비하겠습니다</address>
    </div>
</body>
</html>
</code></pre>

---

Basic CSS Usage:
<pre><code class="language-html">
<ol>
		<li>application</li>
		<li>documentents</li>
		<li>workinterview</li>
</ol>
</code></pre>

---

CSS Selections:
<pre><code class="language-html">
<!DOCTYPE html>
<html>
<head>
    <style>
        #big-title {background-color: indigo; color:whitesmoke}
        #content {background-color: aqua;}
        .title {color: darkgoldenrod;}
        .item {color:yellow; background-color:blue;}
    </style>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>class</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <link rel='stylesheet' type='text/css' media='screen' href='main.css'>
    <script src='main.js'></script>
</head>
<body>
    <div id="big-title">
        <h1>class selection</h1>
    </div>
    <div id="content">
        <p class="title">learned items</p>
        <p class="item">tag selector</p>
        <p class="item">id selector</p>
        <p class="item">class selector</p>
        <hr/>
        <p class="title">unlearned items</p>
        <p class="item">spring</p>
        <p class="item">etc.</p>
    </div>
</body>
</html>
</code></pre>

-gonkgonk
