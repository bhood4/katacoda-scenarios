
Terraform builds a graph of all your resources, and parallelizes the creation and modification of any non-dependent resources. Because of this, Terraform builds infrastructure as efficiently as possible, and operators get insight into dependencies in their infrastructure.

A directed graph of dependencies can be show using the CLI:

`terraform graph`{{execute}}

A image visualizing this can be made using dot:

`terraform graph| dot -Tpng > graph.png`{{execute}}

![example graph.png](/katacoda-scenarios/tf101/assets/graph.png)

