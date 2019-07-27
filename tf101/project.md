Related .tf configuration files for a project are place in a common directory. 
Additional files in the directory include:
* .terraform.d: Folder containing downloaded provider binaries and local state cache
* variables.tf: Consolidated variable initialisation
* outputs.tf: Consolidated outputs
* .tfvars: Variable overrides 

* Keep key components in separate TF project directorys
* Each directory brings a dedicated state file - blast radius stays small
* Follow standardized file naming, e.g. main.tf, varialbes in variables.tf, outputs in outputs.tf

<pre>├── nginx
│   ├── main.tf
│   ├── storage.tf
│   ├── variable_overrides.tfvar
│   └── variables.tf
├── database
│   ├── main.tf
│   ├── mysql.tf
│   ├── variable_overrides.tfvar
│   └── variables.tf
└── network
    ├── main.tf
    ├── net-peering.tf
    ├── variable_overrides.tfvar
    └── variables.tf
</pre>
