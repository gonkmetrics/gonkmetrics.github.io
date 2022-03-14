## JS Functions, Constructors, Events

Today's session was spent on the basics of Javascript.

* Functions
* Local and Global Variables
* Built-in Functions
* Constructors in JS
* Events

---

Functions:

Continuing from last time, functions in JS can be called from anywhere in a document, including the body. Note the function is called for with a return command, such that the element gives the return type in the function.

<pre><code class="language-xml">
&lt;br&gt;&lt;a href=&quot;#&quot; onclick=&quot;return nextPic()&quot;&gt;&amp;gt;&amp;gt;&lt;/a&gt;
</code></pre>

Executes nextPic() after clicking element.

<pre><code class="language-javascript">
var num = 1;
function nextPic(){
    if(num === 3){
        num = 0;
    }
    num++;
    document.getElementById("pic").src = "img/cat" + num + ".jpg";
    return false;
}
</code></pre>

---

Local and Global Variables

Javascript variables have function and global scope, similar to how methods and classes in Java can be public or private. This limits the locations from which a variable can be accessed.

> Local, or function scope variables are only accessed from within their containing function.

<pre><code class="language-javascript">
function theFnc(){
    var num;
    num = 30;
}

theFnc();
console.log(num);
</code></pre>

> Global variables can be called from anywhere but only inherit their value as defined globally. <br> Meaning that a global variable called within a function and modified within the same function does not have their "global" value changed.

<pre><code class="language-javascript">
var num;
function theFnc(){
    num = 30;
}

theFnc();
console.log(num);
</code></pre>

#Note:
Global variables called inside functions essentially exist in two forms: their global var and the var within the function. The same var called in another function retains the values of the global var.

---

Built-in Functions:

Mostly parsers.

<pre><code class="language-javascript">
var result1 = eval("10 + 20;"); //most often can be used to parse strings received from prompts
var num = 100;
document.write("num"+10+"<br>");
document.write(eval("num")+10+"<br>");

var infiniteValue = 1/0;
document.write(infiniteValue+"<br");
var result2 = isFinite(infiniteValue);
console.log(result2);

var result3 = isNaN(1/"a");
document.write(1/"a" + "<br>")
document.write(result3 + "<br>");

todo:

Number()

String()

escape()

unescape()
</code></pre>

---

Constructor:

Constructors are identical to that of Java:

<pre><code class="language-javascript">
//Constructor:
function computer(cpuInfo, ramInfo, ssdInfo){
    this.cpu = cpuInfo;
    this.ram = ramInfo;
    this.ssd = ssdInfo;

    this.totInfo = function(){
        document.write("manufactured by: amd");
        document.write("64bit");

    }
}

//Constructed object:
var myCom2 = new computer("AMD", "16GB", "2TB");
document.write(myCom.cpu + "<br>"+ myCom.ram + "<br>" + myCom.ssd + "<br>");
myCom.totInfo();
</code></pre>

---

Events:

JS events are actions applied to HTML elements that occur when a specified condition occurs. Refer to JS documentation for a full list.

*Crucially*, there are functions events that are sequence-dependent, meaning that they may not activate, unless they are bookended by events, which can activate them at an appropriate time during the runtime.

For instance, the below code reads a value from a tag, but is skipped in execution:

<pre><code class="language-javascript">
var h1Tag = document.getElementsByClassName("noData");
console.log(h1Tag[0]);
</code></pre>

With an event, this command can be executed after the page loads and the tag element is visible.

<pre><code class="language-javascript">
window.onload = function(){
var h1Tag = document.getElementsByClassName("noData");
console.log(h1Tag[0].className);
</code></pre>

---

-gonkgonk
