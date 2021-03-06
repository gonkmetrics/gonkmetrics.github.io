## HTML Form Tags and Groupings

For this session basic HTML was reviewed together with the beginnings of CSS.

Three distinct concepts were covered:

* Additional HTML form tags
* Groupings in HTML
* Basic CSS

---

Additional Form Tags:
There are also various form tags such as "slider", permutations of "date"/"time", and "color". Placeholder values, arguments such as *readonly* and general practice with HTML forms was completed today.

<pre><code class="xml">
&lt;html&gt;
&lt;head&gt;
    &lt;style&gt;
        * { margin : 10px }
    &lt;/style&gt;
    &lt;meta charset=&apos;utf-8&apos;&gt;
    &lt;meta http-equiv=&apos;X-UA-Compatible&apos; content=&apos;IE=edge&apos;&gt;
    &lt;title&gt;formoption3&lt;/title&gt;
    &lt;meta name=&apos;viewport&apos; content=&apos;width=device-width, initial-scale=1&apos;&gt;
    &lt;link rel=&apos;stylesheet&apos; type=&apos;text/css&apos; media=&apos;screen&apos; href=&apos;main.css&apos;&gt;
    &lt;script src=&apos;main.js&apos;&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    disabled:
    &lt;fieldset&gt;
        &lt;legend&gt;writing here:&lt;/legend&gt;&lt;form&gt;
            &lt;p&gt;write: &lt;input type=&quot;text&quot; value=&quot;abcd&quot; readonly/&gt;&lt;/p&gt;
            &lt;p&gt;title: &lt;input type=&quot;text&quot;/&gt;&lt;/p&gt;
            &lt;textarea cols=&quot;30&quot; rows=&quot;10&quot;&gt;&lt;/textarea&gt;
            &lt;input type=&quot;submit&quot; value=&quot;ubit&quot;/&gt;
            &lt;input type=&quot;reset&quot; value=&quot;reset&quot;/&gt;
        &lt;/form&gt;
    &lt;/fieldset&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

<pre><code class="language-html">
&lt;html&gt;
&lt;head&gt;
    &lt;style&gt;
        * { margin : 10px }
    &lt;/style&gt;
    &lt;meta charset=&apos;utf-8&apos;&gt;
    &lt;meta http-equiv=&apos;X-UA-Compatible&apos; content=&apos;IE=edge&apos;&gt;
    &lt;title&gt;formoption3&lt;/title&gt;
    &lt;meta name=&apos;viewport&apos; content=&apos;width=device-width, initial-scale=1&apos;&gt;
    &lt;link rel=&apos;stylesheet&apos; type=&apos;text/css&apos; media=&apos;screen&apos; href=&apos;main.css&apos;&gt;
    &lt;script src=&apos;main.js&apos;&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    disabled:
    &lt;fieldset&gt;
        &lt;legend&gt;writing here:&lt;/legend&gt;&lt;form&gt;
            &lt;p&gt;write: &lt;input type=&quot;text&quot; value=&quot;abcd&quot; readonly/&gt;&lt;/p&gt;
            &lt;p&gt;title: &lt;input type=&quot;text&quot;/&gt;&lt;/p&gt;
            &lt;textarea cols=&quot;30&quot; rows=&quot;10&quot;&gt;&lt;/textarea&gt;
            &lt;input type=&quot;submit&quot; value=&quot;ubit&quot;/&gt;
            &lt;input type=&quot;reset&quot; value=&quot;reset&quot;/&gt;
        &lt;/form&gt;
    &lt;/fieldset&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

<pre><code class="language-xml">
&lt;html&gt;
&lt;head&gt;
    &lt;style&gt;
        * { margin : 10px }
    &lt;/style&gt;
    &lt;meta charset=&apos;utf-8&apos;&gt;
    &lt;meta http-equiv=&apos;X-UA-Compatible&apos; content=&apos;IE=edge&apos;&gt;
    &lt;title&gt;formoption3&lt;/title&gt;
    &lt;meta name=&apos;viewport&apos; content=&apos;width=device-width, initial-scale=1&apos;&gt;
    &lt;link rel=&apos;stylesheet&apos; type=&apos;text/css&apos; media=&apos;screen&apos; href=&apos;main.css&apos;&gt;
    &lt;script src=&apos;main.js&apos;&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    disabled:
    &lt;fieldset&gt;
        &lt;legend&gt;writing here:&lt;/legend&gt;&lt;form&gt;
            &lt;p&gt;write: &lt;input type=&quot;text&quot; value=&quot;abcd&quot; readonly/&gt;&lt;/p&gt;
            &lt;p&gt;title: &lt;input type=&quot;text&quot;/&gt;&lt;/p&gt;
            &lt;textarea cols=&quot;30&quot; rows=&quot;10&quot;&gt;&lt;/textarea&gt;
            &lt;input type=&quot;submit&quot; value=&quot;ubit&quot;/&gt;
            &lt;input type=&quot;reset&quot; value=&quot;reset&quot;/&gt;
        &lt;/form&gt;
    &lt;/fieldset&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

---

Groupings:
Groupings, or <div> tags, more generally, is a core concept in HTML. <div> tags do not have any visual effects on the HTML file, but they allow for blocks of text and tags to be assigned a class or id value that can be called. Additionally, tags themselves can be called, as will be seen with CSS below.

A default layout with groupings would be "header" -> "main" -> "footer", but any <div> tags can be assigned any unique values.

<pre><code class="nohighlight">
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
            <li><a href="#">?????? ??????</a></li>
            <li><a href="#">?????? ??????</a></li>
            <li><a href="#">?????? ??????</a></li>
            <li><a href="#">??????</a></li>
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
        <address>????????? ??? ?????????????????????</address>
    </div>
</body>
</html>
</code></pre>

---

Basic CSS Usage:
CSS can be incorporated within an HTML file, or outside of it. CSS within the body of an HTML file is referred to as inline CSS, and takes the form of the [style] argument within a tag. CSS can also be written into a <style> tag within the header of an HTML file.

An external CSS file can be linked to an HTML file as a stylesheet, or can be called within the <style> block.

<pre><code class="nohighlight">
<head>
    <link rel="stylesheet" href="externalcss.css">

		OR
		<style>
        @import url('externalcs.css');
    </style>

		OR
		<style>
        #big-title {background-color: indigo; color:whitesmoke}
    </style>

		OR
		<body>
		    <div style="border:1px solid red">
		        <div style="color:green">123</div>
		    </div>
		</body>
</code></pre>

---

CSS Selections:
This is where groupings come together with CSS. CSS can be applied to types/tags, to tags with argument [id="name"] referenced by # or [class="name"] referenced by '.'

<pre><code class="nohighlight">
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
