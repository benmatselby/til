# Sort and `uniq` content, and display where count is greater than one

Recently, I needed to find the intersection of two files. One way to do this is to concatenate the files, sort the content, and then use `uniq` to find duplicate lines.

Image I had this content in two files:

```text
# one.txt
Alice
Bob
Jack
```

```text
# two.txt
Alice
```

I know want to get the `uniq` count of names in those files:

```shell
cat one.txt two.txt | sort | uniq -c
  2 Alice
  1 Bob
  1 Jack
```

But, I want to only show where there is an intersection (i.e. count greater than one). I can do this by piping the output to `awk`:

```shell
cat one.txt two.txt | sort | uniq -c | awk -v limit=1 '$1 > limit{print $1" "$2}'
```
