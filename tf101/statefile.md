
* Terraform stores the state of the infrastructure and configuration it has deployed in a file on disk or remote storage
* 1--1 relationship of project to state
* Terraform interrogates the state file to establish diff of current vs desired 
* JSON format, simple to read / validate in tests


* Local state storage is default but only good for single user prototyping
* Use a [https://www.terraform.io/docs/state/remote.html](Remote state backend): 
** artifactory
** azurerm
** consul
** etcd
** etcdv3
** gcs
** http
** manta
** oss
** pg
** s3
** swift
** terraform enterprise
* Lock-aware remote state storage recommended for all but dev/test
* Protect state files and use state versioning - loss of a state != good
