## DOM and Element Creation

Today's session was spent on the last of the basics of Javascript.

* DOM Cont'd
* Creating Elements in JS

---
<br><br>
# DOM Continued:

Recall the following DOM selectors. Remember that the code must be executed after the window loads.

Selects by id attribute in tag.
<pre><code class="language-javascript">var number = document.getElementById("number");
</code></pre>

Selects multiple elements by tag.
<pre><code class="language-javascript">var div1 = document.getElementsByTagName("div");
</code></pre>

Both .children and .childNodes select the child elements of a specified node. *Additionally*, specifying the index by appending .children[index] OR .childNodes[index].
<pre><code class="language-javascript">var div2 = div1[0].childNodes;
var div3 = div1[0].children;
</code></pre>

Recall the other types of selectors that return node:
<pre><code class="language-javascript">console.log(div1[0].firstChild);
console.log(div1[0].lastChild);
console.log(div2[1].previousSibling);
console.log(div1[0].nextSibling);
</code></pre>

.nextElementSibling returns the element, not the node. I.e. no text ("#text") or comment nodes.
<pre><code class="language-javascript">console.log(resetBtn.nextElementSibling);
</code></pre>

Parse integer value from DOM selected element.
<pre><code class="language-javascript">var currentNum = parseInt(number.innerText, 10);
</code></pre>

Then you can change the contents of the DOM selected element.
<pre><code class="language-javascript">number.innerText = currentNum + 1;
</code></pre>

---
<br><br>
# Creating Elements:

Uses function .createElement(arguments). Explained in code comments:

<pre><code class="language-javascript">window.onload = function(){
//Creates tag element from defined string p.
var PTAG = document.createElement("p");

//Any kind of tag element can be created.    
var BUTTON = document.createElement("button");

//Creates #text:
var TEXT = document.createTextNode("button1");

//Sets tag attributes from arguments attribute and attribute content.
BUTTON.setAttribute("id", "button1");

//Appends BUTTON as a child element of PTAG.
PTAG.appendChild(BUTTON);

//Body element has no id, therefore it must be selected:    
var BODY = document.getElementsByTagName("body");

//Appends PTAG as a child element of BODY.
BODY[0].appendChild(PTAG);

//Adds #text to BUTTON element.
BUTTON.appendChild(TEXT);
}</code></pre>

---
<br><br>
# Callbacks:

Referencing the below block of code:

<pre><code class="language-javascript">createh1.onclick = function createTag(){
var h1tag = document.createElement("h1");
var text1 = document.createTextNode("h1 tag");
var hr = document.createElement("hr");
h1tag.appendChild(text1);
h1tag.appendChild(hr);
h1space.appendChild(h1tag);
}</code></pre>

To make this work with callback, add the callback function outside of the window.onload event. Add callback to arguments and callback() to the inside of the event function.

Not tested, but delete the window.onload event as well? Since the function would be loaded after the button anyways. Then set the button to call the functions as attribute onclick="functions(callback function)".

Callback function would be:

<pre><code class="language-javascript">function changeTag() {
h1tag.setAttribute("class", "h1tag");
h1tag.style.color = "blue";
}</code></pre>

Function is called back whenever createTag(changeTag) is executed.


-gonkgonk
