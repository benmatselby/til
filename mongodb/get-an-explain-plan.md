# Get an explain plan for a query

To get an explain plan for a query in MongoDB, you can use the `explain()` method.
This method provides information about the execution of a query, including the
stages of the query and the indexes used.

```shell
db.user.find({status: "active"}).explain()
```
