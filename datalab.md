# GCP datalab

## Setup

Follow the [quickstart](https://cloud.google.com/datalab/docs/quickstart) instructions.

# Datalab in a team environment

* Datalab instances are single-user.
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
