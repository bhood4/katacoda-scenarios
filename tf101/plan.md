Once the configuration has been defined we need to create an execution plan. Terraform describes the actions required to achieve the desired state. The plan can be saved using -out. We'll apply the execution plan in the next step.

To create a plan, use the CLI

`terraform plan -out config.tfplan`{{execute}}

The output of the command indicates the changes. In this case, you'll see a _+ dockercontainer.nginx-server and _+ dockerimage.nginx to highlight adding the new resources. Finally a summary of Plan: 2 to add, 0 to change, 0 to destroy.

