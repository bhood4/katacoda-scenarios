
`cd /root/terraform-learn/aws/environments/dev/networking`{{execute}}


edit terraform.tfvars according to your networking requirements

`terraform init`{{execute}}

`terraform plan -var-file=./terraform.tfvars`{{execute}}

`terraform apply -state=./terraform.tfstate -var-file=./terraform.tfvars`{{execute}}
