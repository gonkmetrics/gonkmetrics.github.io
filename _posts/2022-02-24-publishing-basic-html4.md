## Basic HTML 3

<img src="_img\jake.jpg" style="display: block; margin-left: auto; margin-right: auto; width: 50%;">

This session was packed with fun times trying to make highlight.js work for this blog, as well as figuring out if whitespaces were coming from block elements or dividers. Anyhow.

Two things were covered:

* Even more CSS selection methods
* Fonts

---

Additional CSS Selectors:

Classes, ids, and types can also be relationally selected. Such as selecting everything with [*].
<pre><code class="language-css">
  * {color:blue;}
</code></pre>

Or selecting child types from parent types in the order [PARENT>CHILD]. Note the specificity of the selector, where a selector with a higher specificity takes precedence over a selectors with lower specificity.
<pre><code class="language-css">
  p{color:violet;}

  ul > li > p{color:green;}
</code></pre>

Proximity selections for objects ahead or behind a specified object can also be made with [+].
<pre><code class="language-css">
  h1 + p {color:blue;}

  p + p {color:purple;}
</code></pre>

Combined together, these selections can yield (ugly) results such as these:
<pre><code class="xml">
&lt;html&gt;
&lt;head&gt;
    &lt;style&gt;
        h1{color:blue}
        h1 + p{background-color: lightcoral;}
        /* [id^=&apos;content_&apos;] {font-size:5;} */
        ul {margin-bottom: 0; margin-block-start: 0;}
        #content_A &gt; ul &gt; li{border-style: solid; color: black; border-color: purple;}
        #content_B &gt; ul &gt; li{border-style: solid;color: purple; border-color: green;}
        #content_C &gt; ul &gt; li{border-style: solid;color:pink; border-color: yellow;}
    &lt;/style&gt;
    &lt;meta charset=&apos;utf-8&apos;&gt;
    &lt;meta http-equiv=&apos;X-UA-Compatible&apos; content=&apos;IE=edge&apos;&gt;
    &lt;title&gt;selectorq1&lt;/title&gt;
    &lt;meta name=&apos;viewport&apos; content=&apos;width=device-width, initial-scale=1&apos;&gt;
    &lt;script src=&apos;main.js&apos;&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;div id=&quot;container&quot;&gt;
        &lt;h1&gt;프로그래밍 언어들&lt;/h1&gt;
        &lt;p&gt;프로그래밍 언어들 대해서 &lt;span style=&quot;color:lightpink&quot;&gt;차근차근&lt;/span&gt;...&lt;/p&gt;
        &lt;div id=&quot;main&quot;&gt;
            &lt;div id=&quot;content_A&quot;&gt;
                &lt;ul&gt;
                    &lt;li&gt;
                        &lt;h2&gt;자바&lt;/h2&gt;
                        &lt;span&gt;앱 개발이 모두 됨&lt;/span&gt;
                    &lt;/li&gt;
                &lt;/ul&gt;
            &lt;/div&gt;
            &lt;div id=&quot;content_B&quot;&gt;
                &lt;ul&gt;
                    &lt;li&gt;
                        &lt;h2&gt;파이썬&lt;/h2&gt;
                        &lt;span&gt;머신러닝 등에 특화&lt;/span&gt;
                    &lt;/li&gt;
                &lt;/ul&gt;
            &lt;/div&gt;
            &lt;div id=&quot;content_C&quot;&gt;
                &lt;ul&gt;
                    &lt;li&gt;
                        &lt;h2&gt;C++&lt;/h2&gt;
                        &lt;span&gt;게임개발에 특화&lt;/span&gt;
                    &lt;/li&gt;
                &lt;/ul&gt;
                &lt;!-- do not use div class, put class or id on li tag--&gt;
            &lt;/div&gt;
        &lt;/div&gt;    
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

<pre><code class="language-html">
<html>
<head>
    <style>
        h1{color:blue}
        h1 + p{background-color: lightcoral;}
        /* [id^='content_'] {font-size:5;} */
        ul {margin-bottom: 0; margin-block-start: 0;}
        #content_A > ul > li{border-style: solid; color: black; border-color: purple;}
        #content_B > ul > li{border-style: solid;color: purple; border-color: green;}
        #content_C > ul > li{border-style: solid;color:pink; border-color: yellow;}
    </style>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>selectorq1</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <script src='main.js'></script>
</head>
<body>
    <div id="container">
        <h1>프로그래밍 언어들</h1>
        <p>프로그래밍 언어들 대해서 <span style="color:lightpink">차근차근</span>...</p>
        <div id="main">
            <div id="content_A">
                <ul>
                    <li>
                        <h2>자바</h2>
                        <span>앱 개발이 모두 됨</span>
                    </li>
                </ul>
            </div>
            <div id="content_B">
                <ul>
                    <li>
                        <h2>파이썬</h2>
                        <span>머신러닝 등에 특화</span>
                    </li>
                </ul>
            </div>
            <div id="content_C">
                <ul>
                    <li>
                        <h2>C++</h2>
                        <span>게임개발에 특화</span>
                    </li>
                </ul>
                <!-- do not use div class, put class or id on li tag-->
            </div>
        </div>    
    </div>
</body>
</html>
</code></pre>

Selections can also be made from tag properties:
<pre><code class="language-css">
  h1[class] {color:blue;}
</code></pre>

After selecting an object, virtual selectors can be used for additional effects.
<pre><code class="language-css">
/*
a:hover changes color while being moused over
*/
  a:hover {color:royalblue;}
/*
a:active changes color after being clicked
*/
  a:active{color:salmon;}
/*
a:link changes color after accessing the linked website
*/
  a:link {color:seagreen;}
/*
etc.
*/
  a:visited {color:yellow;}
</code></pre>

There are some additional positional selectors in CSS:
<pre><code class="language-css">
.box:after{
    content: "select";
    color: green;
}
p:first-letter {font-size:300%;}
p {border-bottom: 1px dashed black;}
.box > p:last-child{border:none;}
</code></pre>

And applying to subobjects without [>], provided the selection is nested within.
<pre><code class="language-css">
  .box a:hover{color:gold;}
</code></pre>

Finally, multiple selections:
<pre><code class="language-css">
  p, ul {border: 1px solid blue;}
</code></pre>

---

Fonts:

Multiple parameters exist to modify fonts in CSS:
<pre><code class="language-css">
body {font: 12px , Gulim;}
h1 {
    font-family: Impact;
    font-size: larger;
    font-weight: 200;
    font-style: italic;
    color: blue;
}
p {
    font: bold italic 15px , Gulim;
    color: chartreuse;
}
</code></pre>

Yielding these results:
<pre><code class="language-html">
<html>
<head>
    <style>
        body {font: 12px , Gulim;}
        h1 {
            font-family: Impact;
            font-size: larger;
            font-weight: 200;
            font-style: italic;
            color: blue;
        }
        p {
            font: bold italic 15px , Gulim;
            color: chartreuse;
        }
    </style>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>Page Title</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <link rel='stylesheet' type='text/css' media='screen' href='main.css'>
    <script src='main.js'></script>
</head>
<body>
    <h1>subsidy</h1>
    <p>web app development</p>
</body>
</html>
</code></pre>

Finally, fonts can be imported locally or online, if the default font set is not enough.
<pre><code class="xml">
&lt;html&gt;
&lt;head&gt;
    &lt;style&gt;
        /* use @import to make a selection of fonts available */
        @import url(&apos;https://fonts.googleapis.com/css2?family=Redressed&amp;family=Roboto:wght@100&amp;display=swap&apos;);
        .rob {
            font-family: &apos;Roboto&apos;, sans-serif;
        }

        .arl {
            font-family: &apos;Redressed&apos;, cursive;
        }
    &lt;/style&gt;
    &lt;meta charset=&apos;utf-8&apos;&gt;
    &lt;meta http-equiv=&apos;X-UA-Compatible&apos; content=&apos;IE=edge&apos;&gt;
    &lt;title&gt;Page Title&lt;/title&gt;
    &lt;meta name=&apos;viewport&apos; content=&apos;width=device-width, initial-scale=1&apos;&gt;
    &lt;link rel=&apos;stylesheet&apos; type=&apos;text/css&apos; media=&apos;screen&apos; href=&apos;main.css&apos;&gt;
    &lt;script src=&apos;main.js&apos;&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1 class=&quot;rob&quot;&gt;roboto&lt;/h1&gt;
    &lt;p class=&quot;rob&quot;&gt;roboto roboto&lt;/p&gt;
    &lt;h1 class=&quot;arl&quot;&gt;arial&lt;/h1&gt;
    &lt;p class=&quot;arl&quot;&gt;arial arial&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

<pre><code class="language-html">
<html>
<head>
    <style>
        /* use @import to make a selection of fonts available */
        @import url('https://fonts.googleapis.com/css2?family=Redressed&family=Roboto:wght@100&display=swap');
        .rob {
            font-family: 'Roboto', sans-serif;
        }

        .arl {
            font-family: 'Redressed', cursive;
        }
    </style>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>Page Title</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <link rel='stylesheet' type='text/css' media='screen' href='main.css'>
    <script src='main.js'></script>
</head>
<body>
    <h1 class="rob">roboto</h1>
    <p class="rob">roboto roboto</p>
    <h1 class="arl">arial</h1>
    <p class="arl">arial arial</p>
</body>
</html>
</code></pre>


-gonkgonk
