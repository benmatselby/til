# Job management

You can suspend a current process by running `Ctrl+z`.

```shell
[1]  + 83432 suspended  git diff
```

This drops you back down to your shell prompt.

If you then want to go back to that process, you can run:

```shell
jobs
[1]  + suspended  git diff
```

Now you can resume that suspended process:

```shell
fg %1
```
