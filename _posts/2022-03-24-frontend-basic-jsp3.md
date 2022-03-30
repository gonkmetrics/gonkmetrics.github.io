## Java Server Pages - Request Object

Java (current. Jakarta) Server Pages is a framework used for web application development.

This post will discuss:
* Request Object and Methods

<br>

---
# Request Object
<br>

The request object in JSP is used for:

<ol>
<li>Reading info from the client</li>
<li>Letting the server read info</li>
<li>Reading parameters from a client request</li>
<li>Reading the data on cookies</li>
</ol>

In other words, it deals with the interactions between a client and its server.
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/jsp1.png" style="display: block; margin-left: auto; margin-right: auto;"><br>

>Methods for request object:
>>getContextPath()
<br>Gets the path for the request object.
<br>setMethod();
<br>Sets the method by which the request is communicated.
<br>getServerName():
<br>Gets server name.
<br>getServerPort();
<br>Gets port number.
<br>getRequestURL/URI()
<br>Gets server URL.
<br>getRemoteAddr();
<br>Gets remote address.
<br>getProtocol();
<br>Gets the protocol used. (Between client, server)

<br>
The essential methods for the request object, however, are those that handle data communicated over pages by the request object:
>Methods for request object:
>>getParameter():
<br>Gets the parameters passed by the request, by key/name.
<br>getParameterValues():
<br>Gets all values passed by the request.
<br>getParameterNames():
<br>Gets all keys in enum.
<br>getParameterMap():
<br>Gets map object. Contains the keys and corresponding values.

<br>
The request object is called from inside the document. The input field must specify the *name* and *type* values.
<pre><code class="language-xml">&lt;form action=&quot;recipient_page.jsp&quot; method=&quot;get/post&quot;&gt;&lt;/form&gt;
</code></pre><br>
<br>
And can then be handled. The value of the request is saved to the defined variable.
<pre><code class="language-java">String a = request.getParameter("abc");
</code></pre><br>

<br>

-gonkgonk
