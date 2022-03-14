## HTML Overflows and Positioning

Today's session was spent on methods for layout and positioning.

* Layouts, Wrapping up Floats and Overflows
* Position Property

---

Wrapping up Floats and Overflows:

Floating elements are elements that are floated above other elements to the left or right (horizontal margins). As was defined verbatim in <a href="https://gonkmetrics.github.io/2022/02/28/publishing-basic-html5.html">Blog 7</a>.

The Overflow property in CSS allows elements where content may "overflow" from the borders of an element.

<pre><code class="language-css"><style>
    *{
        margin: 0;
        padding: 0;
    }

    body{
        font: 12px; margin: 10px;
    }

    #container{
        width: 200px;
        height: 100px;
        border: 1px solid #ccc;
        overflow: **scroll/visible/hidden/auto**;
    }
</style>
</code></pre>

All these parameters, aside from [visible] hide overflown content. For reference (and skipping the obvious ones) scroll adds a scrollbar in the direction of the overflown element. Auto defines the overflow behavior to fit the given dimensions of an element.

Combined with floats, overflown text may look like this:
<pre><code class="xml">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;style&gt;
        *{width: 600px; margin: 0; padding: 0;}
        #header{border: 2px dotted red;}
        #body{border: 2px solid blue; display: inline-block; height:fit-content;}
        .contentLeft{
            border: 2px solid gray; width: 25%; height: 300px;
            float: right; overflow: auto;}
        .contentRight{
            border: 2px solid gray; width: 48%; height: 300px;
            float: left;}
        .contentRight&gt;p{overflow-wrap: break-word; width:fit-content;}
        .contentCenter{
            border: 2px solid gray; width: 25%; height: 300px;
            float: left; overflow: hidden;}
        #footer{border: 2px dashed green; height: 100px; clear:both; margin-top: -4px;}
    &lt;/style&gt;
    &lt;meta charset=&#39;utf-8&#39;&gt;
    &lt;meta http-equiv=&#39;X-UA-Compatible&#39; content=&#39;IE=edge&#39;&gt;
    &lt;title&gt;double&lt;/title&gt;
    &lt;meta name=&#39;viewport&#39; content=&#39;width=device-width, initial-scale=1&#39;&gt;
    &lt;link rel=&#39;stylesheet&#39; type=&#39;text/css&#39; media=&#39;screen&#39; href=&#39;main.css&#39;&gt;
    &lt;script src=&#39;main.js&#39;&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;div id=&quot;header&quot;&gt;
        &lt;h1&gt;
            Lorem ipsum
        &lt;/h1&gt;
        &lt;br&gt;
        &lt;p&gt;Consectetur adipiscing elit.&lt;/p&gt;
    &lt;/div&gt;
    &lt;div id=&quot;body&quot;&gt;
        &lt;div class=&quot;contentLeft&quot;&gt;
            &lt;p&gt;
                Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Mauris nec ante ut ligula faucibus tincidunt.
                Nulla ut elit ac ex egestas eleifend.
                Maecenas sit amet est sit amet magna eleifend porta.
                Curabitur at justo eleifend, malesuada sem et, tempus dolor.
            &lt;/p&gt;
        &lt;/div&gt;
        &lt;div class=&quot;contentCenter&quot;&gt;
            &lt;p&gt;
                Suspendisse scelerisque arcu eu est facilisis volutpat.
                Nullam luctus odio hendrerit sem consectetur sodales.
                Aliquam et risus viverra, commodo nisl ac, condimentum dolor.
                Curabitur tristique sapien non elit scelerisque accumsan.
                Maecenas eu tortor sit amet leo scelerisque porta vel eget velit.
            &lt;/p&gt;
        &lt;/div&gt;        
        &lt;div class=&quot;contentRight&quot;&gt;
            &lt;p&gt;
                Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Mauris nec ante ut ligula faucibus tincidunt.
                Nulla ut elit ac ex egestas eleifend.
                Maecenas sit amet est sit amet magna eleifend porta.
                Curabitur at justo eleifend, malesuada sem et, tempus dolor.
            &lt;/p&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    &lt;div id=&quot;footer&quot;&gt;
        &lt;p&gt;
            Praesent non tortor ut metus dignissim pretium.
            Integer congue velit ac metus finibus ultricies.
            Nam pretium orci sit amet enim malesuada sagittis.
            Aenean egestas lacus eget tellus pulvinar rutrum.
            Pellentesque laoreet ipsum sed felis pellentesque dignissim.
        &lt;/p&gt;
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

Note: Text wrapping using the property overflow-wrap only works when the width (limit) is defined for the element. Without it the text **does not** wrap

Yields the (ugly) result:
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/CSSlayout2.png" style="display: block; margin-left: auto; margin-right: auto;">

Positioning using the position property in CSS is done via the properties [bottom/top/right/left] and the parameters for the position property [relative/absolute/static/fixed].

> Relative positioning in CSS positions an element relative to its default position without styling. Therefore an absolute element is moved around it's origin point (0,0) in the default document flow.

> Absolute positioning in CSS positions an element in relation to its parent. It is removed from the normal document flow, instead being positioned relative to the origin point (0,0) of the parent element.

Positioning in CSS requires the exact position of an element to be defined. Therefore, attempts to position elements in relation to all other elements in a document should be done with scripting or functions such as flexbox.

<pre><code class="language-css">#footer{
      position: relative;
      bottom: 0px;
      border: 1px solid green;
  }

  #header{
      border: 1px solid green;
  }

  #container{
      border: 1px solid purple;
  }

  .sidebar{
      border: 1px solid orange;
      position: absolute;
      left: 207px;
      width: 300px;
      height: 322px;
  }

  .content{
      border: 1px solid green;
      position: relative;
      right: 0px;
      width: 194px;
      height: 322px;
  }
  </code></pre>

  Finally, the property z-index can be used to define the layer on which the element is on. The higher the layer number, the greater precedence is given to the element when positioning on the Z-axis.

  <pre><code class="language-css">.element{
    z-index: 1;
  }
  </code></pre>

-gonkgonk
