## Java Server Pages - Session Object

Java (current. Jakarta) Server Pages is a framework used for web application development.

This post will discuss:
* Cookies
* Sessions

<br>



---
# Session
<br>

Sessions are non-persistent objects that exist only when a browser session is active. They are implicit and thus do not need to be constructed unlike cookies. They can inherit values from the client if specified to do so as part of their attributes.

<br>
Cookies and Sessions have similar behavior, with one key difference. Sessions are *non-persistent* and *implicit*, meaning that they automatically are created and then destroyed with every new session of a browser.
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/jsp2.png" style="display: block; margin-left: auto; margin-right: auto;"><br>

>Methods for session object:
>>setMaxAge(seconds)
<br>setPath()
Assigns path for cookie on server.
<br>setValue()
Assigns value field for cookie.
<br>setVersion()
Assigns cookie version.
<br>getMaxAge()
Assigns cookie lifespan.
<br>getName()
Gets cookie name.
<br>getPath()
Gets cookie path.
<br>getValue()
Gets cookie value.
<br>getVersion()
Gets cookie version.

<br>

-gonkgonk
