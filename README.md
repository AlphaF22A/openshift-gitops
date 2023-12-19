# openshift-gitops
An explanation of GitOps &amp; resource files that can be deployed on an OpenShift cluster

GitOps is an operational framework that takes the best practices of DevOps used in application development and applies them to infrastructure management. These aspects of development include version control, collaboration, compliance, and CI/CD.

An application running in a pod in an OpenShift cluster can be provisioned with three files: A deployment configuration file, a service configuration file, and a route configuration file. These three are all in yaml format and can be created manually as a resource via the OpenShift console. Alternatively, a Kustomize file can be used, which pulls a container image from a predefined registry. Both are illustrated below.

![Manual_Container](https://github.com/AlphaF22A/openshift-gitops/assets/88580931/900ebb4e-e20d-407d-80f5-6262187b7a59)
![Manual_Container_K](https://github.com/AlphaF22A/openshift-gitops/assets/88580931/67cf9018-29e6-4ade-9c12-81c3bf33ab2d)
