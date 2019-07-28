Once the configuration has been defined we need to create an execution plan. Terraform describes the actions required to achieve the desired state. The plan can be saved using -out. We'll apply the execution plan in the next step.

To create a plan, use the CLI

`terraform plan -out config.tfplan`{{execute}}

The output of the command indicates the changes. In this case, you'll see a _+ dockercontainer.nginx-server and _+ dockerimage.nginx to highlight adding the new resources. Finally a summary of Plan: 2 to add, 0 to change, 0 to destroy.

* Variables can be overridden using command line arguments
`terraform plan -var 'container_count=5'`{{execute}}

* Alternatively, variables can be overridden using a tfvars file to pass the value.  Here, the file dev.tfvars contains ovrriding variable values:
<pre class="file" data-filename="dev.tfvars" data-target="replace">container_count=3
</pre>

`terraform plan -var-file=dev.tfvars`{{execute}}
