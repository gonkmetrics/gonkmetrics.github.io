## Java Database Connectivity - Basics 2

JDBC is an API that allows access to databases from clients using the Java language.

This post will discuss:
* Example Queries
* PreparedStatement Object

---

# Example Queries
<br>

Queries can be initialized to variables to receive their return values or can be executed standalone with the methods:
<br>

Executes a DDL statement (CREATE, USE) with *bool* return:
<pre><code class="language-java">bool rSetPossible = statement.execute(QUERY);
</code></pre><br>
Executes DML statements (INSERT, UPDATE, DELETE) with *int* return specifying the number of manipulated rows:
<pre><code class="language-java">int row = statement.executeUpdate(QUERY);
</code></pre><br>
Executes statements that return data (SELECT) with return to a ResultSet:
<pre><code class="language-java">ResultSet rS= statement.executeQuery(QUERY);
</code></pre><br>

String form (for reference):

DELETE
<pre><code class="language-java">String ins = "DELETE FROM userinfo WHERE user_id='"+userId+"'";
				stmt.executeUpdate(ins);
</code></pre><br>

INSERT
<pre><code class="language-java">String ins = "INSERT INTO userinfo VALUES ('"+userId+"','"+userPw+"','"+userName+"','"+userEmail+"')";
			stmt.executeUpdate(ins);
</code></pre><br>

UPDATE
<pre><code class="language-java">String ins = "UPDATE userinfo SET user_id='"+userId+"', user_pw='"+userPw+"', user_name='"+userName+"', email='"+userEmail+"' WHERE user_id='"+originalUserId+"'";
			stmt.executeUpdate(ins);
</code></pre><br>

---

# PreparedStatement Object
<br>

SQL statements can be precompiled. *.setObject* methods can be used to set values for parameters marked with **?** that are indexed from n=1. The type of specified object determines the datatype of the inserted value.
<br>

Query has syntax:
<pre><code class="language-sql">STATEMENT FROM table WHERE attribute = ?
</code></pre><br>
Java syntax:
<pre><code class="language-java">PreparedStatement pS = con.prepareStatement(QUERY);
//set value for attributes
pS.setString(1, value);
//execute
pS.execute();
</code></pre><br>

**-gonkgonk**
