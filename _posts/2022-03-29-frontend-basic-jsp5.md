## Java Server Pages - Session Object

Java (current. Jakarta) Server Pages is a framework used for web application development.

This post will discuss:
* Session Object

<br>
---
<br>
# Session
<br>

Sessions are non-persistent objects that exist only when a browser session is active. They are implicit and thus do not need to be constructed unlike cookies. They can inherit values from the client if specified to do so as part of their attributes.

<br>
Cookies and Sessions have similar behavior, with one key difference. Sessions are *non-persistent* and *implicit*, meaning that they automatically are created and then destroyed with every new session of a browser.
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/jsp2.png" style="display: block; margin-left: auto; margin-right: auto;"><br>

Sessions do not need to be constructed. Set the session attributes:
<pre><code class="language-java">session.setAttribute("bc","123");
</code></pre>
<br>
Session values can be grabbed. They are by default type *object*:
<pre><code class="language-java">String session = (String)session.getAttribute("abc");
</code></pre>
<br>
Other session methods can be used for misc. Functionality. The below page redirects if the session is null and kicks out logged in users by parsing for an existing attribute name.
<pre><code class="language-java">    String userId = (String)session.getAttribute("s_id");
    Enumeration<String> attNames = session.getAttributeNames();
    boolean get = attNames.hasMoreElements();
	if(userId!=null){
	}else if(get){
		response.sendRedirect("session_login_ok.jsp");
	}
</code></pre>
<br>

>Methods for session object:
>>setAttribute():
<br>Sets session attributes.
<br>getAttribute():
<br>Gets attributes.
<br>getId():
<br>Gets the session's unique id.
<br>getCreationTime():
vGets the time at which the session was created.
<br>getLastAccessedTime():
<br>Gets the last access time for the session.
<br>set/getMaxInactiveInterval():
<br>Sets/gets the lifetime of the session once it is inactive.
<br>removeAttribute():
<br>Removes specified attribute.
<br>invalidate():
<br>Invalidates, "deletes" the session.

<br>

-gonkgonk
