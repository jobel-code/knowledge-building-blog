# Installing GCP SDK on ubuntu

You have two options,
1. Use package manager `apt-get install google-cloud-sdk`, However, all updates and components installations must use `apt install` instead of `gcloud components install`.
2. Or [download](https://cloud.google.com/sdk/docs/quickstart-linux) the current  `*.tar.gz` file (**RECOMMENDED**). Using this installation I was then able to update and install components by issuing `gcloud components update` or `gcloud components install kubectl datalab`. This option, also solves the error `ERROR: (gcloud.components.install) The component manager is disabled for this installation`.

# Related
Note that `google-cloud-sdk`  can also be installed using `conda install -c bioconda google-cloud-sdk` see: [anaconda_knowHow.md](https://github.com/jobel-code/knowledge-building-blog/blob/master/anaconda_knowHow.md).
