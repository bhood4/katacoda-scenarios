Terraform stores the state of the infrastructure and configuration it has deployed in terraform.tfstate JSON file:

Use the editor tree to the right to view the local terraform.tfstate file.

* The tfstate file can stored a file on disk (local) or remote storage (remote backend)
* 1--1 relationship of project to state
* Terraform interrogates the state file to establish diff of current vs desired 
* JSON format, simple to read / validate in tests
* Local state storage is default but only good for single user prototyping
* Use a [Remote state backend](https://www.terraform.io/docs/state/remote.html): 
(artifactory, azurerm, consul, etcd, etcdv3, gcs, http, manta, oss, pg, s3, swift, terraform enterprise)
* Remote state backend which are lock-aware and support state versioning are recommended 
* Protect state files - loss of a state != good
