# Fix broken access to sudo

Oh, I don't know when this might be handy [[1](./touch-id-for-sudo.md)][[2](./touch-id-for-sudo-with-tmux.md)]!

If you get this error:

```plaintext
sudo: unable to initialize PAM: No such file or directory
```

Do not panic, it is likely that there is some drama with the `/etc/pam.d/sudo_local`
file. I had this when I made a mess of the links above. The file was owned by `root` and I could not `sudo vim` to fix it.

To resolve this, open the folder in the terminal to Finder:

```shell
open /etc/pam.d
```

Then right click on the `sudo_local` file and select "Get Info". In the
"Sharing & Permissions" section, ensure that your user has "Read & Write"
access. If not, change it to "Read & Write". Then edit the file to hopefully
fix the issue.
