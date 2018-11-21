# GCP datalab

## Setup

Follow the [quickstart](https://cloud.google.com/datalab/docs/quickstart) instructions.

# Datalab in a team environment

* instances are **single-user**.
* a recommended practice is to include the user’s name in the name of the instance, so that you can easily associate an instance with a user.


# Create a datalab [source](https://cloud.google.com/datalab/docs/how-to/datalab-team).

- A *project owner* can create a cloud datalab for each team member. Use: `datalab create <instance-name> --for-user <user.email>`
- The *datalab user* must have at least the following IAM roles ():
  - `roles/compute.instanceAdmin.v1`
  - `roles/iam.serviceAccountActor` for the service account attached to the user's Cloud Datalab instance.

**NOTE** The first `datalab create` call per project will try to also create a Cloud Source Repository for sharing notebooks in the project. Since this operation requires owner permissions, an owner must either create the first instance or manually create the `datalab-notebooks` repository in the project. Alternatively, you can disable this behavior by passing in the `--no-create-repository` flag to the create command.

The `datalab create` command also creates the following Google Cloud Platform resources (if not already available):

* The `datalab-network` network
* A firewall rule on the `datalab-network` allowing incoming SSH connections
* The `datalab-notebooks` Google Cloud Source Repository
* The persistent disk for storing Cloud Datalab notebooks


# [Managing the lifecycle of a Cloud Datalab instance](https://cloud.google.com/datalab/docs/how-to/lifecycle).

**Cloud Datalab runs** inside of a **Google Compute Engine VM** with an **attached persistent disk** that is used to store notebooks. Cloud Datalab VMs are connected to a special network in a project called `datalab-network`. The default configuration of this network limits incoming connections to SSH connections.

By default, the `datalab create` command connects to the newly created instance. But, you can use `datalab create --no-connect <instance-name>` and then `datalab connect <instance-name>`. **Note**: The `datalab connect` command restarts your instance if it is not running. The command continues to run until you stop it.

By default, the local port used for the connection is `8081`. To change use: `datalab connect --port 8082 <instance-name>`.

**Avoid incurring unnecessary costs when you want to pause using Cloud Datalab** by `datalab stop <instance-name>`.

# [Updating the Cloud Datalab VM without deleting the notebooks disk](https://cloud.google.com/datalab/docs/how-to/lifecycle#updating_the_cloud_datalab_vm_without_deleting_the_notebooks_disk).

In short do:
```
datalab delete --keep-disk <instance-name>
datalab create <instance-name>
```

**NOTE**: *Notebooks are not copied between zones*. Cloud Datalab VMs are zonal. If you change zones when you re-create the VM, the new VM will get a new Persistent Disk (PD). Your notebooks will not be copied from the PD in the previous zone to the PD in the new zone (to manually copy notebooks from the PD to your local machine, see [Copying notebooks from the Cloud Datalab VM](https://cloud.google.com/datalab/docs/how-to/working-with-notebooks#copying_notebooks_from_the_cloud_datalab_vm)).


# [Deleting an instance and the notebooks disk](https://cloud.google.com/datalab/docs/how-to/lifecycle#deleting_an_instance_and_the_notebooks_disk)

In short:
`datalab delete --delete-disk <instance-name>`

# [Reducing usage of compute resources](https://cloud.google.com/datalab/docs/how-to/lifecycle#reducing_usage_of_compute_resources)

- Stop the datalab instance `datalab stop <instance-name>`. However, You will continue to incur charges for the resources attached to the VM (such as the persistent disk and the external IP address), but the VM instance itself will not incur charges while it is stopped. When you need to use your stopped instance again, run `datalab connect <instance-name>` to connect to your instance, and the datalab tool will restart the instance before attempting to connect to it.
- To **stop incurring all charges** associated with a Cloud Datalab instance, you must delete both the VM and the attached persistent disk by running the `datalab delete` command with the `--delete-disk option`.

# checkout [Colaboratory](https://colab.research.google.com/)
Colaboratory is a research tool for machine learning education and research.

All Colaboratory notebooks are stored in Google Drive. Colaboratory notebooks can be shared just as you would with Google Docs or Sheets. Simply click the Share button at the top right of any Colaboratory notebook, or follow these Google Drive file sharing instructions.
