
Terraform is a go binary CLI and is easy to install and use. The install instructions vary by platform, linux is assumed for this course.  See https://www.terraform.io/downloads.html

## Install terraform 
Download version 0.11.14 linux platform zip, unzip, move to /usr/local/bin

`curl https://releases.hashicorp.com/terraform/0.11.14/terraform_0.11.14_linux_amd64.zip -O; unzip terraform_0.11.14_linux_amd64.zip; rm terraform_0.11.14_linux_amd64.zip; sudo mv terraform /usr/local/bin`{{execute}}

## git clone
`git clone https://github.com/contino/terraform-learn.git`{{execute}}

## setup AWS env

`export AWS_ACCESS_KEY_ID={your_access_key}`{{execute}}
`export AWS_SECRET_ACCESS_KEY={your_secret_key}`{{execute}}
`export AWS_DEFAULT_REGION={your_preferred_region}`{{execute}}
