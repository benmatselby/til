# Find commit where a string was added

So `git blame` will tell you the last person who touched a line of code, but they might not have introduced it. What if you want to know who added the line?

You can use `git log -S` to find the commit that introduced a specific string. For example, if you want to find the commit that added the string "wibble" to your codebase, you can run:

```bash
git log -S 'wibble'
```

If you want to see all changes, you can use `git log -G 'wibble'`
