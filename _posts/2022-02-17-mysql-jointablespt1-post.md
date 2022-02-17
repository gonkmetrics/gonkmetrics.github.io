## MySQL - Joining Tables Pt.1 ft. Blog Creation

MySQL Workbench was used to verify queries before being pasted into the cli.

For this session example tables were joined using the keyword JOIN.

```sql
--Simple Join Query
SELECT *
  FROM userTbl INNER JOIN buyTbl
  ON userTbl.user_id = buyTbl.user_id;
```

To create a static alias for the example tables buyTbl and userTbl I used VIEW objects.

```sql
CREATE VIEW b AS SELECT * FROM buyTbl;
```

Further arguments for the JOIN keyword were also reviewed:

```sql
-- types:
-- INNER returns only matched records
SELECT buyTbl.*, userTbl.user_name, userTbl.phone_num, userTbl.addr
  FROM userTbl
  INNER JOIN buyTbl
  ON userTbl.user_id = buyTbl.user_id;
-- LEFT records from left table + matched records
SELECT *
  FROM student s
  LEFT JOIN membership m
  ON s.user_name = m.user_name;
-- RIGHT records from right table + matched recordsSELECT *
  FROM student s
  RIGHT JOIN membership m
  ON s.user_name = m.user_name;
-- CROSS returns all records
-- CROSS was not reviewed but noted as an argument in my script file
```

Normalization/정규화 was also touched upon for 1st and 2nd normalizations. Higher order normalizations have been added to my list of things to review.

Additionally some initial setup for this blog was finished:

To start the blog I used [chadbaldwin's](https://github.com/chadbaldwin/simple-blog-bootstrap) template.

Jekyll was the recommended option for building a site with mdl. Ruby was installed straight from RubyInstaller and the ruby directory was added to PATH. Jekyll was then installed:

```powershell
gem install jekyll bundler

cd gonkmetrics.github.io

bundle init
```

After adding the required gems (themes, etc.):

```powershell
bundle add webrick

bundle exec jekyll serve
```

Atom was installed and is currently the tool from which I'm blogging.

The root for gonkmetrics.github.io was also locally hosted.

Changes were not tested locally but rather pushed directly from Atom and deployed to the github-site.

-gonkgonk
