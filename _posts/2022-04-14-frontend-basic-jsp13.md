## Java Server Pages - Testing a Servlet with Forms

In application development, common design challenges can be tackled using software design patterns.

This post will discuss:
* Testing a Servlet with forms

---
# A Brief Reminder

GET and POST request methods are illustrated in the below diagram. They are the method by which the servlet can provide responses to requests from the client.
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/jsp8.jpg" style="display: block; margin-left: auto; margin-right: auto;">
<br>

<br>
---
# Testing a Servlet with forms
<br>

The client begins by making a POST request to the server.
<pre><code class="language-xml">&lt;form action=&quot;http://localhost:8080/MyFirstWeb/spring&quot; method=&quot;post&quot;&gt;
&lt;input type=&quot;text&quot; name=&quot;jsp&quot;/&gt;
&lt;input type=&quot;text&quot; name=&quot;boot&quot;/&gt;
&lt;input type=&quot;text&quot; name=&quot;jpa&quot;/&gt;
&lt;input type=&quot;submit&quot;/&gt;
&lt;/form&gt;
</code></pre>
<br>
The servlet receives a POST request and executes the contents of the method *getPost()*.
<pre><code class="language-java">	protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		// TODO Auto-generated method stub
		String formA = request.getParameter("formA");
		String formB = request.getParameter("formB");
		String formC = request.getParameter("formC");

		request.setAttribute("formA",formA);
		request.setAttribute("formB",formB);
		request.setAttribute("formC",formC);

		RequestDispatcher dp = request.getRequestDispatcher("servletForm/springResult.jsp");
		dp.forward(request, response);

	}
</code></pre>
<br>
The servlet redirects to the JSP page specified above. The JSP page displays the received values.
<pre><code class="language-xml">&lt;body&gt;
${formA}&lt;br&gt;
${formB}&lt;br&gt;
${formC}
&lt;/body&gt;
</code></pre>
<br>


**-gonkgonk**
