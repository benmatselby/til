# Move windows between sessions

You may be running multiple sessions in tmux, for example:

```text
(0) + work: 5 windows (attached)
(1) + box: 7 windows
```

I want to move a window from my `work` session, to my `box` session. You can do this with the following command:

```shell
<prefix> :move-window -t box:8
```

This will place the current window in `work` to the 8th window in `box`. You can also use `-s` to specify the source window, for example:

```shell
<prefix> :move-window -s work:3 -t box:8
```
