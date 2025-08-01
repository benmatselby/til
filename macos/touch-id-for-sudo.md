# Use Touch ID for sudo

Thanks to Mark Lightfoot for this.

You can use Touch ID for `sudo` on macOS, which allows you to authenticate with your fingerprint instead of entering your password.

Create a file `/etc/pam.d/sudo_local` with the following content:

```plaintext
auth       sufficient     pam_tid.so
```

This does not work in `tmux`. See [Use Touch ID for sudo in tmux](./touch-id-for-sudo-with-tmux.md) for how to set it up in `tmux`.
