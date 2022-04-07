## Java Server Pages - VO, DAO

In application development, common design challenges can be tackled using software design patterns.

This post will discuss:
* VO, DAO Patterns

---

# VO
<br>

A Value Object, or VO, is an object that holds a value. In the context of transferring data between layers of an application, a VO is a Data Transfer Object, or DTO. While data can be assigned to variables, there are reasons to hold such data in a VO class.

VO classes are created in a EJB (not to be confused with JavaBeans, which are classes containing generic objects and methods that can be imported and used in JSP).
<br>

---

# DAO
<br>

Data Access Objects are those that perform any Create, Read, Update, Delete operations in a database. Shorthand for said operations is CRUD, and they are the basic kinds of operations that can be performed on any database.

Normally, logic in JSP and servlets can be written together. However, for the sake of modularization DAO can be used (at least, in handling DB. Other patterns can be used in other situations).

Normally there is a 1 DAO = 1 DB Table equivalence.

DAOs are able to perform CRUD, set values for objects, or get values from objects and pass them to tables.

When using DAOs, a EJB containing table columns, mappings must be made. This EJB is, simply put, the VO.

DAOs are commonly seen throughout the entire programming stack.

<br>

Java syntax:
<pre><code class="language-java">UserVO user = new UserVO();
//goes to bean in src
bean.setterMethod(resultSet.getString(index));
</code></pre><br>

**-gonkgonk**
