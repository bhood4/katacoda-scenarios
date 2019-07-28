
Variables are inputs to the terraform configuration 

<pre class="file" data-filename="variables.tf" data-target="replace">variable "container_count" {
 type = number
 description = "The number of nginx containers to run"
 default = 1
}
</pre>

* resources can access variables in HCL:
<pre>count = "${var.container_countainer_count}"</pre>

* variables must be initialised before they are used (or defaulted).

* Variables can be overridden using command line arguments
`terraform plan -var 'container_count=5'`{{execute}}

* Alternatively, variables can be overridden using a .tfvars file to pass the value
<pre class="file" data-filename="dev.tfvars" data-target="replace">container_count=3
</pre>

`terraform plan -var-file=dev.tfvars`{{execute}}
