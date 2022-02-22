## Basic HTML 1

For this session basic HTML was reviewed again.

Eight distinct concepts were covered:

* Lists
* Tables
* Functions for Forms (Fieldsets)

---

Lists:
Lists have syntax <li> and are ordered in DOWNARDS order. Lists can be nested into each other and different kinds of lists can be used within each other.

Ordered Lists present the elements of the list with a number.
```HTML
<ol>
		<li>application</li>
		<li>documentents</li>
		<li>workinterview</li>
</ol>
```

Unordered Lists present the elements of the list with bullet points. The shape of the bullet points can be specified with argument [type="shape"], with possible options CIRCLE, DISC, SQUARE.
```HTML
<ul type="square">
                    <li>ceo statement</li>
                    <li>ceo about</li>
                    <li>ceo organizational info</li>
                    <li>ceo vision statement</li>
                </ul>
```

Definition Lists present elements in terms of term/name <dt> and an accompanying description <dd>. They are bookended by <dl>.
```HTML
<dl>
		<t1>title is tag dt</t1>
		<dd>definition written with tag dd</dd>
</dl><br>
<dl>
		<dt>syllabus</dt>
		<dd>HTML</dd>
		<dd>CSS</dd>
		<dd>JS</dd>
		<dd>Java</dd>
		<dd>JSP</dd>
		<dd>Spring</dd>
</dl>
```

---

Tables:
Tables have syntax <table> and ordered from LEFT to RIGHT, then DOWNWARDS order. <table> defines a table element, followed by columns <tr> and within row elements, column elements <td>. Arguments for table style can also be defined within the <table> tag, such as [border="N"].

```HTML
<h2>2 by 3 table</h2>
<table border="1">
		<tr>
				<td>1,1</td>
				<td>1,2</td>
				<td>1,3</td>
		</tr>
		<tr>
				<td>2,1</td>
				<td>2,2</td>
				<td>2,3</td>
		</tr>
</table>
```

To create columns that span multiple rows or columns, the <th ARGUMENTS> tag is used. A tag only needs to be written once, from the cell location in which the merged cell starts.
```HTML
<tr>
      <td>어린이</td>
      <th colspan="2">보호자 동반시 무료</th>
</tr>
<tr>
      <th rowspan="2">공연시간</th>
      <td>1회</td>
      <td>12-14시</td>
</tr>
```

---

Forms and Fieldsets:
Forms can be created using HTML, and are written within the tag <fieldset>, which groups form elements together.

A few such elements are shown below:
```HTML
<fieldset>
		<legend>user registration</legend>
		<p>id: <input type="text"/></p>
		<p>password: <input type="password"/></p>
		<p>receieve emails from admin
				<input type="radio" name="recieve">yes
				<input type="radio" name="recieve">no
				<!-- name denotes a pair or group of radio buttons. if they have
				multiple names, then they can be independently selected-->
		</p>
		<p>select account options:
				<input type="checkbox" name="opt" />hide name from online users
				<input type="checkbox" name="opt" />enable private messaging
				<input type="checkbox" name="opt" />do not receive push updates
		</p>
		<p>send:
				<input type="submit" value="submit registration"/>
				<input type="reset" value="cancel registration"/>
				<input type="button" value="save incomplete registration form"/>
		</p>
</fieldset>
```

Fieldsets can also include text input elements. Text boxes are created using the following tags. Arguments [cols] and [rows] define the size of the text box.
```HTML
<textarea cols="30" rows="10"></textarea>
```

Dropdown menus/Selections are also <fieldset> elements. Their syntax is similar to that of lists.
```HTML
<select>
		<optgroup label="markup languages">
				<option>markdown</option>
				<option>html</option>
				<option>json</option>
		</optgroup>
	 <optgroup label="coding languages">
				<option>java</option>
				<option>ruby</option>
				<option>python</option>
	 </optgroup>
</select>
```

Some additional elements introduced in HTML5 include the below.
```HTML
<fieldset>
		<legend>additional elements</legend>
		<form>
				<p>search: <input type="search"/></p>
				<p>email: <input type="email"/></p>
				<p>site address: <input type="url"/></p>
				<p>phone: <input type="tel"/></p>
				<p>age: <input type="number" min="0" max="150"/></p>
		</form>
</fieldset>
```

-gonkgonk
