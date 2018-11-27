a # running jupyter as background and logging
`nohup jupyter notebook > jupyter-nohup.log &`


# Installing google colabtools
`pip3 install git+https://github.com/googlecolab/colabtools.git@master`



# Using `apache-airflow`

# tutorials:
[See source](https://airflow.apache.org/installation.html)

[airflow-tutorial 2 years ago latest commit on 27Jul 2018](https://github.com/hgrif/airflow-tutorial)


`conda install dask`

```
What Unidecode provides is a middle road: function unidecode() takes Unicode data and tries to represent it in ASCII characters (i.e., the universally displayable characters between 0x00 and 0x7F), where the compromises taken when mapping between two character sets are chosen to be near what a human with a US keyboard would choose.
```
# So it will be available before installing airflow
`conda install unidecode`

# TRY FIRST WITHOUT SUDO
`AIRFLOW_GPL_UNIDECODE=yes pip3 install apache-airflow[gcp_api]`

or  using `sudo`
`sudo AIRFLOW_GPL_UNIDECODE=yes pip3 install apache-airflow[gcp_api]`


# Initiating Airflow Database
## [See source](https://airflow.apache.org/installation.html)
Airflow requires a database to be initiated before you can run tasks. If you’re just experimenting and learning Airflow, you can stick with the default SQLite option. If you don’t want to use SQLite, then take a look at Initializing a Database Backend to setup a different database.

## change the default location ~/airflow if you want:
# $ export AIRFLOW_HOME="$(pwd)"

**note** Airflow will use the directory set in the environment variable `AIRFLOW_HOME` to store its configuration and our SQlite database. This directory will be used after your first Airflow command. If you don't set the environment variable AIRFLOW_HOME, Airflow will create the directory `~/airflow/` to put its files in.

`airflow initdb`


# Create your DAG definition file

## IMPORTANT: the DAG definition file IS NOT a place where you can do some actual data processing. The script’s purpose is to define a DAG object.  

One thing to wrap your head around (it may not be very intuitive for everyone at first) is that this Airflow Python script is really just a configuration file specifying the DAG’s structure as code. The actual tasks defined here will run in a different context from the context of this script.
Different tasks run on different workers at different points in time, which means that this script cannot be used to cross communicate between tasks. Note that for this purpose we have a more advanced feature called XCom.
