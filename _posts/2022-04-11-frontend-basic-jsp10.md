## Java Server Pages - Singleton Pattern

In application development, common design challenges can be tackled using software design patterns.

This post will discuss:
* Singleton Pattern

---

# Singleton Pattern
<br>

A common software design problem is the need to create only one of an object. This is most common in systems that break with any different amount of a specific object, and less commonly, to prevent bloat created by additional instances of an object.
<br>
**Singleton Pattern in DAO**
<br>
A multi-page application can either have multiple instances of a DAO created (one per page), or, alternatively, can make use of the singleton pattern.

This means that one instance of the DAO is created, and pages can only access the DAO through a getter method. Only a single DAO is constructed in this case.

<pre><code class="language-java">private static UserDAO dao = new UserDAO();

private UserDAO() {
  try {
    Context ct = new InitialContext();
    ds = (DataSource)ct.lookup("java:comp/env/jdbc/mysql");
  }catch(Exception e) {}
}

public static UserDAO getInstance() {
  if(dao == null){
    dao = new UserDAO();
  }
  return dao;
}
</code></pre>
<br>

Note the scope for UserDAO has gone from *public* to *private*, meaning that the corresponding *getInstance()* method must be used to get the DAO.
<br>

Prior to using this pattern:
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/jsp6.jpg" style="display: block; margin-left: auto; margin-right: auto;">
<br>

After using this pattern. Note the simplified DAO and Connection logic:
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/jsp7.jpg" style="display: block; margin-left: auto; margin-right: auto;">
<br>
**Connection Pool**
<br>
Yet another example of a singleton pattern solution. Instead of creating a *Connection* per page, a connection pool is used.

To make a connection pool, use the DataSource class.
<pre><code class="language-java">private DataSource ds;
private UserDAO() {
  try {
    Context ct = new InitialContext();
    ds = (DataSource)ct.lookup("java:comp/env/jdbc/mysql");
  }catch(Exception e) {}
}
</code></pre>
<br>

Any connections can be made using:
<pre><code class="language-java">con=ds.getConnection();
</code></pre>
<br>

This obliviates the need to close most *Connection* objects, so there is less need to "religiously write" Connection.close();


**-gonkgonk**
