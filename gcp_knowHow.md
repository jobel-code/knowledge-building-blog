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

## Create datalake bucket

- See **[regions and zones](https://cloud.google.com/compute/docs/regions-zones/)**

` gsutil mb -p [PROJECT_NAME] -c [STORAGE_CLASS] -l [BUCKET_LOCATION] gs://[BUCKET_NAME]/`

[STORAGE_CLASS] = Multi-Regional  [LOCATION] 'eu'
                  Regional [LOCATION] 'europe-west1' (Belgium) includes GPUs and cloud functions
                  Regional [LOCATION] 'europe-north1' (Finland) limited services.
```
# Imports the Google Cloud client library
from google.cloud import storage
# Instantiates a client
storage_client = storage.Client()
#
Bucket = storage.bucket.Bucket(client=storage_client, name =bucket_name)
Bucket.storage_class = "MULTI_REGIONAL"
bucket = Bucket.create(location='eu')

```

# Install the Firebase SDK for python
pip install firebase-admin
conda install markdown
pip install google-cloud-firestore
See also (https://googleapis.github.io/google-cloud-python/latest/firestore/index.html)[https://googleapis.github.io/google-cloud-python/latest/firestore/index.html#]

# From zero to jupyterhub in gcp
[https://z2jh.jupyter.org/en/stable/google/step-zero-gcp.html](https://z2jh.jupyter.org/en/stable/google/step-zero-gcp.html)

# Enter a name for your cluster
```
CLUSTERNAME=<YOUR-CLUSTER-NAME>

gcloud beta container clusters create $CLUSTERNAME \
  --machine-type n1-standard-2 \
  --num-nodes 2 \
  --cluster-version latest \
  --node-labels hub.jupyter.org/node-purpose=core

```

To test if your cluster is initialized, run:
`kubectl get node`

# Enter your email
```
EMAIL=

kubectl create clusterrolebinding cluster-admin-binding \
  --clusterrole=cluster-admin \
  --user=$EMAIL

```
# Now setup jupyterhub
