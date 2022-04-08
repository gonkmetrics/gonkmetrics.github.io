## Java Server Pages - Applying VO, DAO 2

In application development, common design challenges can be tackled using software design patterns.

This post will discuss:
* Applying VO, DAO contd.

---

# Applying VO and DAO contd.
<br>

The entire bulk of scriptlet code can be replaced with these design patterns:

First, a page that displays a table containing information from the SQL query:
<pre><code class="language-sql">SELECT * FROM userinfo;
</code></pre><br>

The previously seen code is written in the DAO class:
>>highlightjs is broken:
public class DAO{
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


<br>

And called in the JSP page:
<pre><code class="language-java">&lt;%
UserDAO dao = new UserDAO(); //constructor executes commands in constructor
List&lt;UserVO&gt; userList = dao.getAllUserList(); //execute dao method for class UserDAO
System.out.println(userList);
for(UserVO board : userList){ %&gt;
&lt;tr&gt;
&lt;td&gt;
&lt;%= board.getUserId() %&gt;
&lt;/td&gt;
&lt;td&gt;
&lt;%=  board.getUserPw() %&gt;
&lt;/td&gt;
&lt;td&gt;
&lt;%= board.getUserName() %&gt;
&lt;/td&gt;
&lt;td&gt;
&lt;%= board.getEmail() %&gt;
&lt;/td&gt;
&lt;/tr&gt;
&lt;% } %&gt;
</code></pre>
<br>

<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/jsp4.jpg" style="display: block; margin-left: auto; margin-right: auto;"><br>

Avoiding scriptlets, the below JSTL code is identical in function:
</code></pre>
<br>

And called in the JSP page:
<pre><code class="language-xml">&lt;c:forEach items=&quot;${userList}&quot; var=&quot;element&quot;&gt;
&lt;tr&gt;
&lt;td&gt;&lt;c:out value=&quot;${element.getUserId}&quot;/&gt;&lt;/td&gt;
&lt;td&gt;&lt;c:out value=&quot;${element.getUserPw}&quot;/&gt;&lt;/td&gt;
&lt;td&gt;&lt;c:out value=&quot;${element.getUserName}&quot;/&gt;&lt;/td&gt;
&lt;td&gt;&lt;c:out value=&quot;${element.getEmail}&quot;/&gt;&lt;/td&gt;
&lt;/tr&gt;
&lt;/c:forEach&gt;
</code></pre>
<br>

JSTL searches for the setter/getter methods.

<br>

___
<br>
Another application of the patterns:
<pre><code class="language-java">    String insertU = null;
    String insertP = null;
    String redirectURL = null;
	/* Handle request */
    String formUserId = request.getParameter("userId");
    String formUserPw = request.getParameter("userPw");
    /* DB connection */
	UserDAO dao = new UserDAO();
    UserVO user = dao.getUserInfo(formUserId);
    insertU = user.getUserId();
    insertP = user.getUserPw();

    if((formUserId.equals(insertU))&&(formUserPw.equals(insertP))){
    	session.setAttribute("s_id",formUserId);
    	redirectURL = "loginWelcome.jsp";
    } else if((formUserId.equals(insertU))&&(!(formUserPw.equals(insertP)))){
    	redirectURL = "userPwFail.jsp";
    } else if(!(formUserId.equals(insertU)) || (insertU == null)){
    	/* pass if Id null or incorrect */
    	redirectURL = "userIdFail.jsp";
    }
    response.sendRedirect(redirectURL);
</code></pre>
<br>

Note that while the comparison logic remains the same, the data (business-side) logic is hoisted completely off to their respective classes.
<br>

An unrelated use of the patterns can also be seen in the below diagram (including code):
<img src="https://raw.githubusercontent.com/gonkmetrics/gonkmetrics.github.io/main/_posts/_img/jsp5.jpg" style="display: block; margin-left: auto; margin-right: auto;"><br>


**-gonkgonk**
