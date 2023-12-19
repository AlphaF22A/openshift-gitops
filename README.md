# openshift-gitops
An explanation of GitOps &amp; resource files that can be deployed on an OpenShift cluster

GitOps is an operational framework that takes the best practices of DevOps used in application development and applies them to infrastructure management. These aspects of development include version control, collaboration, compliance, and CI/CD.

An application running in a pod in an OpenShift cluster can be provisioned with three files: A deployment configuration file, a service configuration file, and a route configuration file. These three are all in yaml format and can be created manually as a resource via the OpenShift console. Alternatively, a Kustomize file can be used, which pulls a container image from a predefined registry. Both are illustrated below.

The Kustomize file, or the set of three files (deployment configuration, service, route), may be referenced as an ApplicationSet file which is recognized by Kubernetes. The ApplicationSet file can also be placed onto a central repository which developers and administrators can collaborate and make changes as needed. Upon inputting the ApplicationSet file in the OpenShift console, OpenShift/Kubernetes will create the necessary resources to have a fully functioning container/pod. The diagrams below illustrate as such.

While the following allows for close collaboration and version control, it still requires manual deployment and synchronization of each application in their unique branches, a process which would be time consuming and tedious. As such, one can place the unique ApplicationSet files into a GitHub repository folder, which is referenced by ArgoCd. This process is illustrated below.

Upon referencing the folder and triggering the deployment in ArgoCD, all the resources required by the various branches are provisioned in the cluster for fully functioning containers with their respective applications inside. The details of resource provisioning can be edited and synced with ArgoCD, allowing for further collaboration, version control, and CI/CD.
