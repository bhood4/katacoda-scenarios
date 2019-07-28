
`cd /root/terraform-learn/aws/environments/dev/networking`{{execute}}


open and edit terraform.tfvars according to your networking requirements
run command export AWS_ACCESS_KEY_ID={your_access_key}
run command export AWS_SECRET_ACCESS_KEY={your_secret_key}
run command export AWS_DEFAULT_REGION={your_preferred_region}

`terraform get`{{execute}}

`terraform plan -var-file=./terraform.tfvars`{{execute}}

`terraform apply -state=./terraform.tfstate -var-file=./terraform.tfvars`{{execute}}
