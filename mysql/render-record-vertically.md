# Render a record vertically

Sometimes you want to see a record in MySQL rendered vertically, especially if it has many columns. You can do this using the `\G` command at the end of your query.

```sql
mysql> select User, Host from user\G
*************************** 1. row ***************************
User: root
Host: %
*************************** 2. row ***************************
User: mysql.infoschema
Host: localhost
```
