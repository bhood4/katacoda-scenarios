Terraform works based on a configuration file, in this case config.tf. The configuration defines your infrastructure, in this instance as providers and resources. Terraform looks for all files that have a .tf extension.

A provider is an abstract way of handling the underlying infrastructure and responsible for managing the lifecycle of a resource.

A resource are components of your infrastructure, for example a container or image.

You can use any editor to write the config.tf file. The first section defines a docker provider with the host where we want to apply our configuration too.

provider "docker" {
  host = "tcp://docker:2345/"
}

We can now start defining the resources of our infrastructure. The first resource is our Docker image. A resource has two parameters, one is a TYPE and second a NAME. The type is docker_image and the name is nginx. Within the block we define the name and tag of the Docker Image.

resource "docker_image" "nginx" {
  name = "nginx:1.11-alpine"
}

We can define our container resource. The resource type is docker_container and name as nginx-server. Within the block we set the resource parameters. We can reference other resources, such as a the image.

resource "docker_container" "nginx-server" {
  name = "nginx-server"
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

