# Render a record vertically

By default, SQLite displays records in a tabular format. However, if you want to
see a record rendered vertically, especially when it has many columns, you can
use the `.mode` command to change the output format.

```sql
.mode line
```

```sql
sqlite> select * from feeds;
      id = 4
     url = https://www.theguardian.com/uk/rss
   title = The Guardian
added_at = 2025-07-31 20:53:18.59036+00:00
```

To go back to the default tabular format, you can set the mode back to `table`:

```sql
.mode table
```
