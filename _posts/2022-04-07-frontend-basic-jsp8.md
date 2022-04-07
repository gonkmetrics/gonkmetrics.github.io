## Java Server Pages - Applying VO, DAO

In application development, common design challenges can be tackled using software design patterns.

This post will discuss:
* Applying VO, DAO

---

# Applying VO
<br>

As explored previously:
<pre><code class="language-java">UserVO user = new UserVO();
//goes to bean in src
bean.setterMethod(resultSet.getString(index));
</code></pre><br>

The VO itself is constructed and its getter/setters called. In any case, the VO exists as an object with the sole purpose of holding values from a table. It holds a single row.

As it only holds (with get/set functionality), its function is extended through use in:
<br>

---

# Applying DAO
<br>

DAOs are objects that hold tables from databases. Their value lies in their ability to be commonly used across an application, by different languages, and keeps the "business-side" ops outside of the JSP.

The DAO class can conveniently include the methods and constructors needed to CRUD a table. Therefore, connections and queries are written as part of the DAO, such that when methods and constructors from DAO are called, they are imported and executed from that class.

<br>

Java syntax:


**-gonkgonk**
