## Java Server Pages - Applying VO, DAO 1

In application development, common design challenges can be tackled using software design patterns.

This post will discuss:
* Applying VO, DAO

---

# Applying VO
<br>

A VO class should be created, and the variables it holds defined. Getter/Setter methods should also be created in the class, as these will be used to initialize, modify, and read the VO's values.

As explored previously:
<pre><code class="language-java">UserVO user = new UserVO();
//goes to bean in src
bean.setterMethod(resultSet.getString(index));
</code></pre>

The VO itself is constructed and its getter/setters called. In any case, the VO exists as an object with the sole purpose of holding values from a table. It holds a single row.

As it only holds (with get/set functionality), its function is extended through use in:
<br>

---

# Applying DAO
<br>

DAOs are objects that hold tables from databases. Their value lies in their ability to be commonly used across an application, by different languages, and keeps the "business-side" ops outside of the JSP.

The DAO class can conveniently include the methods and constructors needed to perform CRUD on a table. Therefore, connections and queries are written as part of the DAO, such that when methods and constructors from DAO are called, they are imported and executed from that class.

The DAO class is structured as such:
>>public class DAO{
  private Variables;
  public DAO{
    Class.forName(dbInfo);
  }
  //the below method creates a list that contains VO objects with values from a table
  public List<VO> getAllVO(){
    Connection con = null;
    PreparedStatement pSt = null;
    ResultSet rSt = null;
    List<VO> listVO = new ArrayList<>();
    String query = "query";
    try{
    }catch(Exception e){} finally{
      con.close();
      pSt.close();
      rSt.close();
      //in try-catch block
    }
    return listVO;
  }
}

Now that a DAO class exists, we can call it wherever its needed.

<pre><code class="language-java">DAO dao = new DAO(); //default constructor with commands executed
List<VO> listFromTable = dao.getAllVO(); //method from class DAO. no parameters

</code></pre>

Now a list with VOs from a table exists in the environment where the above code was executed.

<br>



**-gonkgonk**
