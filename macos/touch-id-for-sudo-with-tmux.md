# Use Touch ID for sudo in tmux

See [Use Touch ID for sudo](macos/touch-id-for-sudo.md) for the basic setup.

Follow the instructions from the [pam_reattach repo](https://github.com/fabianishere/pam_reattach)

As of August 2025, it looks like this:

```shell
brew install pam-reattach
```

Then, create/update `/etc/pam.d/sudo_local` with the following content:

```plaintext
auth       optional       /opt/homebrew/lib/pam/pam_reattach.so
```

`optional` means if there are any issues with the Touch ID authentication, it
will fall back to the password prompt.

Ensure that this line is above the line that contains `pam_tid.so`.
