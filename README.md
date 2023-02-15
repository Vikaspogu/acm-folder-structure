# ACM Folder Structure

This repository demonstrates the structuring of the folders to manage configuration for multi-cluster environments using ACM and ArgoCD.

There are three primary folders at the root level.

```text
bootstrap
hubcluster
managedclusters
provision
```

The `bootstrap` folder contains the configuration to create an OpenShift GitOps operator and an instance in the hub cluster. This folder also consists of ApplicationSet to manage lab and prod `hubcluster` applications in an apps-of-apps pattern.

`hubcluster` folder contains the configuration for resources that are created on `hubcluster`

`managedcluster` folder contains the configuration for different environments, i.e., lab, non-prod, and prod; a configuration that gets applied to specified clusters like ARO and AWS; and a standard configuration that is used in all the clusters that are part of the `clusterset` i.e., lab, non-prod, and prod

The `provision` folder contains an Ansible playbook to deploy the OpenShift GitOps operator and instance and create the hub cluster Argo apps of apps.
