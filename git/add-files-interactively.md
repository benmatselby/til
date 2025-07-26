# Add files interactively

If you want to add files to the staging area interactively, you can use the `git add -i` command.
This command allows you to select which changes you want to stage.

Another way you can do this is by using `git add -p`, which allows you to stage
changes in a patch-like manner.

This is handy if you have multiple changes in a file and you want to stage only
some of them. This aides the concept of [Logically atomic commits](https://benmatselby.dev/post/logical-commits/).
