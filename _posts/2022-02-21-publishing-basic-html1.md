## Basic HTML 1

For this session basic HTML was reviewed. VS was used as the IDE as opposed to Atom. Atom will probably still be used for the foreseeable future until I manage to connect VS to git.

Eight distinct concepts were covered:

* Inline/Block Elements
* Paragraph Tags
* Address Tags
* Rule Breaks
* Quotation Tags
* Text Elements
* Embedded Images
* Link Tags/Hyperlinks

---

Inline/Block Elements:
Inline elements and block elements are separated by their need for implicit/explicit use of breaks. Without breaks, inline elements continue on the same line, while block elements are spaced vertically by default.

---

Paragraph Tags:
Paragraph tags are indented block elements that usually represent paragraphs.

```HTML
<h1>Paragraph format</h1>
<p>
		Paragraphs use tag p, which is a block tag<br>
		so they skip lines
</p>
```
---

Address Tags:
Address tags add disclaimer, address, or misc. information at the bottom of a webpage.

```HTML
<address>
        &#60; Seoul, 654 Street &#62;
        031-00-4567
        COPYRIGHT &copy;
        All Rights Reserved
        &lt; TestCode
        <!-- &#60; is < and &#62; is >
        HTML special characters can be typed out with their codes
        some characters are allocated a code so that they don't conflict with
        existing HTML syntax
        -->

    </address>
```
---

Rule Breaks:
Rule Breaks are plain horizontal times used as thematic separators: as demonstrated plainly in this blog post.

```HTML
<h1>horiz line</h1>
    <hr/>
    <p>Horizontal lines are thematic separators, i.e. a literal line on
        the page that separates content
    </p>
    <hr>
    <p>JS uses dynamic elements for this ^</p>
```
---

Quotation Tags:
Quotation Tags delineate long-form quotes. Ideally. They can be used for any kind of quotes, though.

```HTML
<h1>&lt;blockquote&gt; and &lt;q&gt;</h1>
<h2>&lt;blockquote&gt;element</h2>
<p>Poem Lyrics</p>
<blockquote>
		Baba
		Yaga
		Mama
		Zaza
		Papa
</blockquote>
<h2>&lt;p&gt; element</h2>
<p>author: <q>bongus</q></p>
```
---

Text Elements:
Text Elements, or just a fancy way of saying "formatting rules". There are headers <h>, <emphasis> and <strong>, <bold>, and <sub/sup> just to name a few. Being familiar with mdl, these were easy to get used to.

```HTML
<h1>text elements</h1>
<h2>highlighting</h2>
<p>now <em>HTML</em> programming</p>
<p>real <strong>HTML</strong> programming</p>
<h2>two lines of pure programming</h2>
<p><abbr title="Real Programming Hours">RPH</abbr></p>
```
---

Embedded Images:
Self explanatory, really. Parameters such as HxW can be specified in the arguments for the tag.

```HTML
<br><img width="400px" height="400px" src="img\dog.jpg">
```
---

Link Tags/Hyperlinks:
Another self-explanatory-pie. The address is specified as an argument, and can also be used to jump around in a page if the locations are set up and specified.

```HTML
<a href="https://www.youtube.com/">Youtube</a>
<a href="https://www.netflix.com/">Netflix</a>
<a href="https://www.spotify.com/">Spotify</a>

<br><br>

<a href="https://www.youtube.com/">Youtube</a><br>
<a href="https://www.netflix.com/">Netflix</a><br>
<a href="https://www.spotify.com/">Spotify</a>
```

That's all (for today), folks!

-gonkgonk
