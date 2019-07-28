
`cd /root/terraform-learn/aws/environments/dev/compute`{{execute}}

open terraform.tfvars and enter a value for variables vpc_id and subnet_id from the networking infrastructure you have previously built, owner and ssh_key_name (the name of the key associated with your AWS account), and save
run command export AWS_ACCESS_KEY_ID={your_access_key}
run command export AWS_SECRET_ACCESS_KEY={your_secret_key}
run command export AWS_DEFAULT_REGION={your_preferred_region}

`terraform get`{{execute}}

`terraform plan -var-file=./terraform.tfvars`{{execute}}

`terraform apply -state=./terraform.tfstate -var-file=./terraform.tfvara`{{execute}}

