
`cd /root/terraform-learn/aws/environments/dev/compute`{{execute}}

open terraform.tfvars and enter a value for variables vpc_id and subnet_id from the networking infrastructure you have previously built, owner and ssh_key_name (the name of the key associated with your AWS account), and save

`terraform init`{{execute}}

`terraform plan -var-file=./terraform.tfvars`{{execute}}

`terraform apply -state=./terraform.tfstate -var-file=./terraform.tfvara`{{execute}}

