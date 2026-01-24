# Unset an environment variable

When you start a tmux session, it inherits environment variables from your shell. These variables are stored in the tmux server's global environment and are passed to new windows and panes.

The problem arises when you unset a variable in your shell (e.g., `unset ANTHROPIC_API_KEY`). This only affects your current shell process. The tmux server still has the variable in its environment, so any new windows or panes will still receive it.

This is particularly concerning for sensitive data like API keys that you may have temporarily exported and then tried to remove.

## Solution

To properly remove an environment variable from tmux, use:

```shell
tmux set-environment -gu ANTHROPIC_API_KEY
```

The flags mean:

- `-g` - Apply to the global environment (affects all sessions)
- `-u` - Unset the variable

You can verify the variable is gone by listing tmux's environment:

```shell
tmux show-environment -g
```
