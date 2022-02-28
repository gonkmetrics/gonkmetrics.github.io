## Basic HTML 5

Today's session was spent on one concept, with most of the time being dedicated to prototyping.

A central component of CSS was covered:

* Floating Elements

---

Floating Elements:

Floating elements are elements that are floated above other elements to the left or right (horizontal margins).

<pre><code class="language-css">.textblock {
  float: left/right/center;
}
</code></pre>

Elements defined with [Clear] are moved such that they do not overlap with floating elements.

<pre><code class="language-css">.aftertextblock {
  clear:left/right/both;
}
</code></pre>

Together these can create horizontally ordered elements:

<pre><code class="language-css">.header {
    background-color: rgb(207, 207, 207);
    padding: 15px;
    text-align: center;
    letter-spacing: 5px;
}

.intro{
    text-align: center;
}

p:not(.intro){
font-size: 0.8em;
text-align: justify;
}

ul{
    list-style-type: none;
}

li{
    float:left;
    width:20%;
    padding-inline: 10px;
}

h1:not(.header){
    text-align: center;
    color: white;
    padding: 20px;
}

.tulip>h1{
    background-color: lightcoral;
}

.jebi>h1{
    background-color: lightblue;
}

.pumpkin>h1{
    background-color: lightsalmon;
}

.sunflower>h1{
    background-color: lightgreen;
}
</code></pre>

Yielding the following result together with html code:
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/CSSlayout1.png" style="display: block; margin-left: auto; margin-right: auto;">

Floating blocks may potentially collapse, as is their intended behavior. To prevent this, there are three solutions:

<ul>
<li>Create a virtual element with the :after suffix to create a virtual table.</li>
<li>Create an empty html tag. For its css attributes add [clear:both].</li>
<li>In the container element, define height.</li>
</ul>

Finally, [display] can also be used to manipulate layout by changing the behavior of certain elements.

<pre><code class="language-css">#gnb li{
      display:inline;
  }
</code></pre>

-gonkgonk
