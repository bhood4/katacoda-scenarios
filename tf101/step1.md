Terraform is a tool from Hashicorp which enables you to safely and predictably create, change, and improve infrastructure. It is an open source tool that codifies APIs into declarative configuration files that can be shared amongst team members, treated as code, edited, reviewed, and versioned.

With terraform, you Define infrastructure as code to increase operator productivity and transparency.
Terraform provides an elegant user experience for operators to safely and predictably make changes to infrastructure, with a provider model to support unified management approach and workflow across cloud services. Common Terraform configurations can be packaged as modules and used across teams and organizations.

Terraform is a go binary CLI and is easy to install and use. The install instructions vary by platform, linux is assumed for this course.

## Download the linux zip with terraform client, unzip and put in /usr/local/bin

`curl https://releases.hashicorp.com/terraform/0.12.5/terraform_0.12.5_linux_amd64.zip -O; unzip terraform_0.12.5_linux_amd64.zip; rm terraform_0.12.5_linux_amd64.zip; sudo mv terraform /usr/local/bin`{{execute}}

## confirm terraform version
`terraform version`{{execute}}

## terraform help
`terraform `{{execute}}

You can find more about terraform on the official Hashicorp Terraform site at [https://www.terraform.io/](https://www.terraform.io)
