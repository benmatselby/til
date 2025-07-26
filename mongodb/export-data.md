# Export data from MongoDB

To export data from MongoDB, you can use the `mongoexport` command. This command
allows you to export data from a MongoDB collection into a JSON or CSV file.

```shell
mongoexport --db=my-database --collection=user --type=csv --fields=_id \
  --query='{"status": "active"}' --out=/tmp/users.csv $MONGO_URI
```
