## BOM/DOM Selections

Today's session was spent on the basics of Javascript.

* BOM
* DOM

---

# BOM:

The Browser Object Model organizes browser elements:

> BOM objects are the following: *window* and child objects document, navigator, location, screen, and history.
>> BOM objects can be used as targets for functions: open, alert, prompt, confirm, setTimeout, setInterval.

---

Navigator Object:

The navigator object gives information about the browser. Note the possible classes: appName, appVersion, userAgent, etc.

<pre><code class="language-javascript">document.write("name"+navigator.appVersion+"<br>")
OR
document.write("name"+navigator.userAgent+"<br>")
</code></pre>

Will present:
>nameMozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/98.0.4758.102 Safari/537.36

appName is Mozilla, appVersion is 5.0, userAgent is Chrome/98 and associated info.

---

Location Object:

The location object gives information about the URL or current address.

Either display information (such as URL) from the location object:
<pre><code class="language-javascript">document.write("href: " + location.href + "<br>");
</code></pre>

Or change it; the below sets the URL to google.com, acting as a redirect.
<pre><code class="language-javascript">location.href="https://www.google.com";
</code></pre>

---

Screen Object:

The screen object gives information about the browser window.

The below gives height and width. Can be used to dynamically change elements based on screen dimensions.
<pre><code class="language-javascript">document.write(screen.availHeight);
document.write(screen.availWidth);
</code></pre>

---

History Object:

The history object is the record of pages visited in the browser.

The .back, .forward, and .go(n) functions allow for the scripting to redirect to a previous or next page. Below, the buttons are set up to go to the next or last page.
<pre><code class="language-xml">
<input type="button" value="previous page" onclick="history.back();" />
<input type="button" value="next page" onclick="history.go(1);" />
<input type="button" value="forward page" onclick="history.forward();" />
</code></pre>

---

# DOM:

The Document Object Model deals with the document object within the browser, i.e. the HTML. The DOM is a tree hierarchy, with elements being relationally organized as parent-children.

Selections with DOM:

Within the DOM hierarchy elements can be selected in multiple ways:

getElementById selects an element based on it's id inside the tag. This selects the first id in the hierarchy.
<pre><code class="language-javascript">
var myObj = document.getElementById("title");
console.log(myObj);


//changes object style
myObj.style.color = "blue";
</code></pre>

getElementsByTagName gets an element and it's children, organized into arrays. Functions .children, etc. allow for finer selections of subnodes.
<pre><code class="language-javascript">
var myList = document.getElementsByTagName("ul");

//selects child node at index 2
//console.log(myList[1].childNodes[2]);
//selects all child nodes
//console.log(myList[1].children);
//selects first child, only type
//console.log(myList[1].firstChild);
</code></pre>


-gonkgonk
