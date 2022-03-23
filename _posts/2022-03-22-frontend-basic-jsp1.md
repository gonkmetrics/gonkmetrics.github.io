## Jakarta Server Pages - Basic Terms, Related Tags (Scriplets and Declarations)

Jakarta (form. Java) Server Pages is a framework used for web application development.

This post will discuss:
* Basic Terms
* JSP HTML Form Tags

<br>

---
# Basic Terms
<br>
**JSP, Servlets**
As previously stated, JSP is used for web application programming. It can make use of the whole range of Java language functions, and runs separately from the directly client-facing components. (HTML, etc.)

JSP code is run in a Java servlet. Consequently, an implementation of a servlet must be made available to run JSP, such as Apache Tomcat. (Jetty, etc.)

**HTTP**

HTTP is a protocol, part of the application layer (OSI), wherein clients make requests to a server, which then delivers requested resources and content.

Requests that are routed from the client through HTTP can be transferred to a servlet.

**URL**

The URL can be understood as a web address, which points to a web resource on a network. If the address is prepended with the famous *www*, then it points to a resource on the World Wide Web.

The URL is a subset of the URI, which defines the location of a anything - in the context of the internet, it points to resource on a network. The URI includes the URL and the actual URI of a requested resource (defined through port number of a server, path of a resource, or query data).

The <span style="color:blue;">URL</span> and <span style="color:red;">data URI</span> to this blog's repo is:
<span style="color:blue;">https://github.com/gonkmetrics/gonkmetrics.github.io/blob/main/index.md</span><span style="color:red;">#resources</span>

The URL defines the web address needed for a client to connect to a specific server through HTTP.

<br>

---
# JSP HTML Form Tags
<br>
Implementing JSP into a web document can be done inline by inserting JSP code into the web document, delineating it with its own form tags.

**&lt;% %&gt;**
Scriptlet tags delineate Java code to be executed at runtime (page load as well).

<pre><code class="language-xml">	&lt;h2&gt;multiplication tables&lt;/h2&gt;
	&lt;%
	int count = 1;
	while(count &lt; 10){
		for(int mult = 1;mult&lt;=9;mult++){
			if(mult % 2 == 1){
				out.println(&quot;&lt;p&gt;&quot;+count+&quot;*&quot;+mult+&quot;=&quot;+(2*mult)+&quot;&lt;/p&gt;&quot;);
			}
		}
		count++;
	}
	%&gt;
</code></pre>
<br>

**&lt;%! %&gt;**
Declarative tags surround Java code that is declared once on runtime.

<pre><code class="language-xml">	&lt;%!
	//%! declarative
	//% script read
	public int i = 10;
	public String str = &quot;hello&quot;;
	int add(int n1, int n2){
		return n1+ n2;
	}

	%&gt;
	&lt;%
	//declarations
	int result = add(10,5);
	out.println(result);
	out.println(add(16, 14));
	out.println(result);

	%&gt;
</code></pre>
<br>


-gonkgonk
