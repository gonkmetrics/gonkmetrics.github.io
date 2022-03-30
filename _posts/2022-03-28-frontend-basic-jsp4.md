## Java Server Pages - Response Object, Cookie Object

Java (current. Jakarta) Server Pages is a framework used for web application development.

This post will discuss:
* Redirects
* Cookies

<br>

---
# Redirects
<br>

The *response* object has multiple methods for page response behavior.

>Methods for cookie object:
>>setPath():
<br>Assigns path for cookie on server.
<br>setValue():
<br>Assigns value field for cookie.
<br>setVersion():
<br>Assigns cookie version.
<br>getMaxAge():
<br>Assigns cookie lifespan.
<br>getName():
<br>Gets cookie name.
<br>getPath():
<br>Gets cookie path.
<br>getValue():
<br>Gets cookie value.
<br>getVersion():
<br>Gets cookie version.

>*response.sendRedirect(URL)* can be assigned an absolute or relative address.
<br>

---
# Cookies
<br>

Cookies are blocks of HTTP data that persist in the client. Cookies are made in the server and saved client-side. The server can read these cookies on the client and can modify them. They can exist locally and persist.

Cookies can be up to 4 KB in size, and are allotted 50 per domain.
<br>
The constructor for cookies is as follows:
<pre><code class="language-java">Cookie cookie = new Cookie("abc", "123");
</code></pre>
<br>
Cookies are added:
<pre><code class="language-java">response.addCookie(cookie);
</code></pre>
<br>
Cookies can be deleted after selection:
<pre><code class="language-java">    		cookies[c].setMaxAge(0);
    		response.addCookie(cookies[c]);
</code></pre><br>

A *for* loop may be used to select from an array of cookies, as multiple cookies may be used in a domain.

<br>
As the below diagram shows, cookies are stored locally for use by the servlet when responding to client requests. Any data (*fruit* in diagram) can be saved to the cookie.
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/jsp2.png" style="display: block; margin-left: auto; margin-right: auto;"><br>

>Methods for cookie object:
>>setPath():
<br>Assigns path for cookie on server.
<br>setValue():
<br>Assigns value field for cookie.
<br>setVersion():
<br>Assigns cookie version.
<br>getMaxAge():
<br>Assigns cookie lifespan.
<br>getName():
<br>Gets cookie name.
<br>getPath():
<br>Gets cookie path.
<br>getValue():
<br>Gets cookie value.
<br>getVersion():
<br>Gets cookie version.

<br>

-gonkgonk
