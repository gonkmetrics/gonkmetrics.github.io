## Basic Javascript 2

Today's session was spent on the basics of Javascript.

* Loops Contd.
* Time Constructor (Objects)
* Math Constructor
* String Constructor
* Array Constructor

---

Loops Continued:

This involved more review of previous Java concepts.

> Break and Continue statements work identically as they do in Java. Or any C language. Remember, Continue skips once cycle of the loop, ignoring code below the continue statement.

Unrelated to the above, the following is practice with FOR loops. Not being able to directly look at the console makes this process harder.

<pre><code class="language-javascript">
var level = prompt("단수를 입력하세요");
for(var count = 1; count <= level; count++){
    for(var star = 1; star <= count; star++){
        document.write("*");
    }
    document.write("<br>");
}
</code></pre>

---

Time Constructor:

Like Java, Javascript has several util Classes which extend its functionality. The first one to look at is the time Class. Using a constructor we can use it within a document.

<pre><code class="language-javascript">
//#Constructor for the Date methods:
var today = new Date();

//Gets full 4-digit year value
var nowYear = today.getFullYear();

//Gets 2-digit month value
var nowMonth = today.getMonth() + 1;

//Gets full system date value
var nowDate = today.getDate();

//Gets the 0-6 value of the day in the week
var nowDay = today.getDay();

//Gets 24-hr format hour value
var nowHours = today.getHours();

//Gets 60-min format minute value
var nowMinutes = today.getMinutes();

//Gets 60-sec format second value
var nowSeconds = today.getSeconds();

//Gets unix time in ms
var nowTime = today.getTime();

</code></pre>

---

Math Constructor:

Again, like Java, JS has a math Class with several methods:

<pre><code class="language-javascript">
var maxNum = Math.max(30, 70 ,5);
document.write(maxNum);
//Fetches max value from input

var minNum = Math.min(8, 7 ,5);
document.write(minNum);
//Fetches min value from input

var roundNum = Math.round(3.49);
document.write(roundNum);
//Rounds input bidirectionally

var ceilNum = Math.ceil(3.1);
document.write(ceilNum);
//Rounds input up

var floorNum = Math.floor(5.9);
document.write(floorNum);
//Rounds input down

var absNum = Math.abs(-10);
document.write(absNum);
//Absolute value

var ranNum = Math.random();
document.write(ranNum);
//RNG

//Example: RNG that selects a picture from folder /img with filename catN.jpg
var ranNum = Math.floor((Math.random()*3)+1);
document.write('<img src="img/cat'+ranNum+'.jpg">')
</code></pre>

---

String Constructor:

Methods are identical to that of Java:

<pre><code class="language-javascript">
var str1 = new String("javascript");
var str2 = "javascript";
var text = "java is good";
document.write(text.bold() + "<br>");
document.write(text.link("https://www.naver.com") + "<br>")
document.write(text.length + "<br>");
document.write(text.toLocaleLowerCase() + "<br>");
document.write(text.toUpperCase() + "<br>");
document.write(text.indexOf("i") + "<br>");
document.write(text.lastIndexOf("i") + "<br>");
document.write(text.substring(4, 6) + "<br>");
document.write(text.substr(10, 3) + "<br>");
document.write(text.replace("good", "great") + "<br>");
document.write(text.concat("...") + "<br>");
document.write(text.split(" ") + "<br>");
document.write(text.charAt(5) + "<br>");
</code></pre>

Briefly:
<ul>
<li>Bold bolds input.</li>
<li>Link inserts a hyperlink.</li>
<li>Length prints the string length.</li>
<li>toLowerCase changes the string to lowercase.</li>
<li>toUpperCase changes the string to uppercase.</li>
<li>indexOf(string) fetches the index of the first string component.</li>
<li>lastIndexOf(string) fetches the index of the last string component.</li>
<li>Substring concatenates between input indices.</li>
<li>Replace is direct string replacement.</li>
<li>CharAt(index) prints character a position N.</li>
</ul>

---

Array Constructor:

Arrays are constructed and values inputted into them in three ways:

> array[index] = input
> array[index] = [input elements, input elements]
> constructor = new Array(input elements, input elements)

Format for the array constructor is as below:

<pre><code class="language-javascript">
var nameList = new Array();
</code></pre>

---

-gonkgonk
