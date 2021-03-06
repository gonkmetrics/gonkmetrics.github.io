## Java Server Pages - Application Object and Error Pages

Java (current. Jakarta) Server Pages is a framework used for web application development.

This post will discuss:
* Application Object
* HTTP Response Codes and Error Pages

---
<br>
# Application Object
<br>

The Application object in JSP is an implicit server-side (servlet) object that can be called from any client instance. It has get, set, remove methods.

>Methods for application object:
>>setAttribute("attr","value"):
<br>Sets attribute.
<br>getAttribute("attr"):
<br>Gets attirubte value.
<br>removeAttribute("attr"):
<br>Removes specified attribute.
<br>getAttributeNames():
<br>Gets attribute names as enum.

<br>
To illustrate it's scope,
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/jsp3.png" style="display: block; margin-left: auto; margin-right: auto;"><br>
<br>

---
<br>
# Exception/Error Pages
<br>

All web servers will return HTTP responses for requests, and may sometimes return error codes. The web server will respond with an HTTP error code, wrapped in it's own page depending on the server software. If the response page presents the page code, this may be an undesirable behavior, as it exposes code to the client.

>Error Codes:
>>404:
<br>Page not found. Resource does not exist.
<br>500:
<br>Internal server errors.
<br>200:
<br>Request succeeded.
<br>307:
<br>Temporary redirect.
<br>400:
<br>Client error, bad request.
<br>405:
<br>Method not supported for the resource.
<br>503:
<br>Server down.

To redirect to any specific page beyond the server software's default, define this in the directive tag.
<pre><code class="language-java"><%@ page errorPage="error_page.jsp">
</code></pre>
For the page that is landed on:
<pre><code class="language-java"><%@ page isErrorPage="true">
</code></pre>
<br>

-gonkgonk
