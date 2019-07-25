As our infrastructure grows and changes, terraform will manage and ensure we always have our defined desired state.

We can change our container to launch two instances, each with different names.

resource "docker_container" "nginx-server" {
  count = 2
  name = "nginx-server-${count.index+1}"
  image = "${docker_image.nginx.latest}"
  ports {
    internal = 80
  }
  volumes {
    container_path  = "/usr/share/nginx/html"
    host_path = "/home/scrapbook/tutorial/www"
    read_only = true
  }
}
If we create a plan you will see the actions Terraform will need to apply to adapt our infrastructure to match our configuration.

terraform plan -out config.tfplan

The plan will outline the changes. Because we're changing the name and adding a resource we'll see Plan: 1 to add, 1 to change, 0 to destroy.

In the details it will explain that changing a container name forces the resource to be recreated name: "nginx-server" => "nginx-server-1" (forces new resource) along with adding the new container _+ dockercontainer.nginx-server.1

We can then apply the plan as we did in the previous step.

`terraform apply`{{execute}}


