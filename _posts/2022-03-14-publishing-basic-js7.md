## jQuery Events and Effects

Today, jQuery was used together with JS events and effects.

* jQuery + Events
* jQuery + Effects

---
<br>
# jQuery + Events

Standard JS Events can be used with jQuery selections.

>Syntax is SELECTOR.EVENT(FUNCTION{})

Executes CSS function upon click:
<pre><code class="language-javascript">$("#btn1").click(function(){
$("#textZone").css("color", "blue");
});
</code></pre>

Multiple events can be bound to a single function, executing it whenever either of the events occurs:
<pre><code class="language-javascript">$("#btn3").bind("mouseover focus", function(){
$("#textZone").css({"color":"green", "font-weight":"bold"});
});
</code></pre>

A hiding menu dependent on mouse positioning can be implemented with related concepts, in either of two ways:

An event that hides the menu on .mouseenter and hides it once .mouseleaves:
<pre><code class="language-javascript">$("#listWrap").mouseenter(function(){
$(".list1").css({"display":"block"});
});

$("#listWrap").mouseleave(function(){
$(".list1").css({"display":"none"});
});
</code></pre>

Or an event+function that uses the hover method, executing functions on ==true and ==false:
<pre><code class="language-javascript">$(".hover").hover(function(){
//mouse is hovering
$(".hover").css("display","block");
}, function(){
//mouse is not hovering
$(".hover").css("display","none");
});
</code></pre>

---
<br>
# jQuery + Effects

Most importantly, this concept introduces arrow functions:

>Function syntax accepts any {} as a function.
>>$SELECTION => {}

Effects can be chained with jQuery selections as well:

Hide and Show Effects:
<pre><code class="language-javascript">$("#btn1").click(function(){
$(".box1").hide("slow");
});
$("#btn2").click(function(){
$(".box1").show("slow");
});
</code></pre>

Simple Hide/Show Toggle:
<pre><code class="language-javascript">$("#btn3").click(function(){
$(".box2").toggle();
});
</code></pre>

Slide Up Hide and Slide Down Show Effects:
<pre><code class="language-javascript">$("#btn4").click(function(){
$("#btn4").parent().next().slideUp();
});
$("#btn5").click(function(){
$("#btn4").parent().next().slideDown();
});
</code></pre>

Fade In and Out Effects:
<pre><code class="language-javascript">$("#btn8").click(function(){
$("#btn8").parent().next().fadeIn();
});
$("#btn7").click(function(){
$("#btn7").parent().next().fadeOut();
});
</code></pre>

Fade Toggle Effect:
<pre><code class="language-javascript">$("#btn9").click(function(){
$("#btn9").parent().siblings().fadeToggle();
});;
</code></pre>

FadeTo Effect:
<pre><code class="language-javascript">$("#btn11").click(function(){
$("#box3").fadeTo("SPEED", "OPACITY");
});
</code></pre>

-gonkgonk
