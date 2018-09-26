# Installing GCP SDK on ubuntu

You have two options,
1. Use package manager `apt-get install google-cloud-sdk`, However, all updates and components installations must use `apt install` instead of `gcloud components install`.
2. Or [download](https://cloud.google.com/sdk/docs/quickstart-linux) the current  `*.tar.gz` file (**RECOMMENDED**). Using this installation I was then able to update and install components by issuing `gcloud components update` or `gcloud components install kubectl datalab`. This option, also solves the error `ERROR: (gcloud.components.install) The component manager is disabled for this installation`.
