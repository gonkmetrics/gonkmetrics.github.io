## Java Server Pages - MVC, Servlet Creation and Methods

Many web applications make use of the MVC Model 2 design pattern, which separates the user from the server-side and business logic.

In the context of web applications, the user is the browser client, which sends requests to the controller on the server side, or the *servlet*.


>A request is forwarded using the GET or POST method. For multi-page applications.


The controller instantiates, then forwards the contents of the requests to the model, or the *Bean, EJB* in the context of web apps in Java. The bean carries out the functionality needed to fulfill the client's request. This is also the point at which resources such as databases are used.


>The request is parsed and a bean is instantiated, then forwarded to the model. The most simple implementation is to use the request and session objects, using the .setAttribute method to forward information to the view.


Finally, the results are presented as a view, or the *JSP* document. The client receives a response and is presented with commands, to display a JSP document with the results of the fulfilled client request.


>Provided the document is using a bean, JSTL, or EL for output, the session attributes can be fetched and displayed.


This post will discuss:
* Servlet Creation, Methods

---
# Servlet Creation, Methods

Servlets can be defined as many things, but in this context, it is the controller component of an MVC Model 2 scheme. The servlet can be created in Eclipse through *New → Create Servlet*.

The servlet class inherits from the abstract class HttpServlet.

The servlet may be accessed through a corresponding URL mapping, and may include various methods. The contents of a servlet class are below:
<pre><code class="language-java">/**
 * Servlet implementation class Servlet
 */
@WebServlet("/pageA") //www.localhost:8181/MyFirstWeb/apple
public class Servlet extends HttpServlet {
	private static final long serialVersionUID = 1L;

    /**
     * @see HttpServlet#HttpServlet()
     */
    public Servlet() {
        super();
        // TODO Auto-generated constructor stub
    }

	/**
	 * @see Servlet#init(ServletConfig)
	 */
	public void init(ServletConfig config) throws ServletException {
		//AFTER SERVLET IS INSTANTIATED, CODE IN INIT IS EXECUTED
	}

	/**
	 * @see Servlet#destroy()
	 */
	public void destroy() {
		//WHEN TIME EXCEEDS MAXTIME IN CONTEXT.XML, THE SERVLET EXPIRES
	}

	/**
	 * @see HttpServlet#doGet(HttpServletRequest request, HttpServletResponse response)
	 */
	protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
    //ON RECEIVING A GET REQUEST, EXECUTES CODE IN BODY
	}

	/**
	 * @see HttpServlet#doPost(HttpServletRequest request, HttpServletResponse response)
	 */
	protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
    //ON RECEIVING A POST REQUEST, EXECUTES CODE IN BODY
	}

}
</code></pre>
<br>


**-gonkgonk**
