Terraform is a go client binary used to perform Infrastructure As Code to managem cloud resources.

## Get the zip file with the terraform go client, unzip and put in /usr/local/bin

`curl https://releases.hashicorp.com/terraform/0.11.13/terraform_0.11.13_linux_amd64.zip -O; unzip terraform_0.11.13_linux_amd64.zip; rm terraform_0.11.13_linux_amd64.zip; sudo mv terraform /usr/local/bin`{{execute}}

## confirm terraform is installed and see the version
`terraform version`{{execute}}

## terraform commands
`terraform `{{execute}}

An example of the current step is `katacoda-scenario-examples/create-scenario-101/step1.md`{{open}}

The JSON file defines the scenario title, the description, steps order, the UI layout and environment. You can find more about the layouts within our scenarios at [katacoda.com/docs/scenarios/layouts](https://katacoda.com/docs/scenarios/layouts) and environments at [katacoda.com/docs/scenarios/environments](https://katacoda.com/docs/scenarios/environments).
