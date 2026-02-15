# Change the port when running via Brew

If you run Jenkins via Homebrew and want to change the port, edit the following file:

```text
/opt/homebrew/opt/jenkins-lts/homebrew.jenkins-lts.service
```

Find and replace `8080` with the port you want, and then restart the service:

```shell
brew services restart jenkins-lts
```
