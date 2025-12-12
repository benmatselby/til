# Finding a window

You may be running multiple tmux sessions, each with multiple windows. To find a specific window across all sessions, you can use the following command:

```tmux
<prefix> :find-window wibble
```

Or

```tmux
<prefix> f
```

Both of these options will filter the list of windows to those matching "wibble". You can then navigate through the filtered list to select the desired window.

To provide a full list of windows without filtering, you can use:

```tmux
<prefix> w
```

From here you will get a list that will provide keyboard shortcuts to quickly navigate to the desired window.

Lastly, you can run:

```tmux
<prefex> '
```

Here you can then type the name of a window within the current session to quickly switch to it.
