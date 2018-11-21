# Installing GCP SDK on ubuntu

You have two options,
1. Use package manager `apt-get install google-cloud-sdk`, However, all updates and components installations must use `apt install` instead of `gcloud components install`.
2. Or [download](https://cloud.google.com/sdk/docs/quickstart-linux) the current  `*.tar.gz` file (**RECOMMENDED**). Using this installation I was then able to update and install components by issuing `gcloud components update` or `gcloud components install kubectl datalab`. This option, also solves the error `ERROR: (gcloud.components.install) The component manager is disabled for this installation`.

# Related
Note that `google-cloud-sdk`  can also be installed using `conda install -c bioconda google-cloud-sdk` see: [anaconda_knowHow.md](https://github.com/jobel-code/knowledge-building-blog/blob/master/anaconda_knowHow.md).

However, you need to keep only one installation, either *GCP on ubuntu* or *using the anaconda bioconda package*.

# Best practices

* keep only one `GCP SDK` installation. Do not duplicate by using `conda install ...`.

# Create the service account key
[SEE:](https://cloud.google.com/docs/authentication/production#auth-cloud-implicit-python)

## GCP console

- go to [Create service account key page](https://console.cloud.google.com/)

## Command line <USE THIS>

`gcloud iam service-accounts create [NAME]`

`gcloud projects add-iam-policy-binding [PROJECT_ID] --member "serviceAccount:[NAME]@[PROJECT_ID].iam.gserviceaccount.com" --role "roles/owner"`

`gcloud iam service-accounts keys create [FILE_NAME].json --iam-account [NAME]@[PROJECT_ID].iam.gserviceaccount.com`

**mv `[FILE_NAME].json`** it to YOUR secure `.config/`

**linux**  edit .bashrc
`export GOOGLE_APPLICATION_CREDENTIALS="[PATH]"`

**windows with `PowerShell`**
`$env:GOOGLE_APPLICATION_CREDENTIALS="[PATH]"`
