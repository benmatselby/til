# Authenticate with `gcloud`

When using Google Kubernetes Engine (GKE), you often need to authenticate your `kubectl` command-line tool with Google Cloud to manage your Kubernetes clusters. This is typically done using the `gcloud` command-line tool.

## Install gcloud CLI

Install the SDK

`brew install google-cloud-sdk`

## Add to shell configuration file

For me, this is adding to `~/.zshrc`

```text
source "$(brew --prefix)/share/google-cloud-sdk/path.zsh.inc"
source "$(brew --prefix)/share/google-cloud-sdk/completion.zsh.inc"
```

Then we can initialise `gcloud init`

## Authenticate

Get credentials for the clusters in different projects ([documentation](https://cloud.google.com/kubernetes-engine/docs/how-to/cluster-access-for-kubectl)):

- `gcloud components install gke-gcloud-auth-plugin`
- `gcloud container clusters get-credentials [gcloud-project] --region=europe-west1`
- `kubectl get pods` - (optional: testing it generally works)
- `kubectl get nodes` - (optional: testing it generally works)
