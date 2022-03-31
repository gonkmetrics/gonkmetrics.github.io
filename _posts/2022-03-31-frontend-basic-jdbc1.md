## Java Database Connectivity - Basics: DriverManager Interface/Connection/Statement/ResultSet Objects and Methods

JDBC is an API that allows access to databases from clients using the Java language. It relies on the specific Connector to be available from the DB.

This post will discuss:
* Basics

---
<br>
# JDBC Functionality
<br>

The libraries associated with connecting to the DB must be installed in order for it to be usable. Connector/J is the one used with JDBC.

<br>
JDBC allows the client running Java to interface with a DB. The parameters specify a MySQL (com.mysql) & (jdbc:mysql) DB will be accessed.
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/jdbc1.png" style="display: block; margin-left: auto; margin-right: auto;"><br>
<br>

JDBC commands can be executed within a try-catch block as SQL exceptions are checked exceptions - so it's easier to figure what goes wrong w/ then.

Returns the interface *Driver* associated with the contained parameter.
<pre><code class="language-java">Class.forName("com.mysql.cj.jdbc.Driver");
</code></pre><br>
Create the object *Connection* to handle the connection with the DB.
<pre><code class="language-java">Connection con = DriverManager.getConnection("jdbc:mysql://address:port/schema?serverTimezone=UTC","username","password");
</code></pre><br>
Create the object Statement to handle commands written in Java.
<pre><code class="language-java">Statement statementA = con.createStatement();
</code></pre><br>
Create the ResultSet object, which contains the table with the queried data.
<pre><code class="language-java">ResultSet resultSet = statementA.executeQuery("QUERY");
</code></pre><br>
The .next method both moves to the next row in the table, while also functioning as a conditional, where *true* if the next row exists and *false* when it does not.
<pre><code class="language-java">resultSet.next();
OR
statement(resultSet.next()){
  ...
}
</code></pre>
<br>

-gonkgonk
