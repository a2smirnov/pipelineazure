# Azure DevOps pipeline test
# Push with tags containing 'Build' string triggers app deployment at azure k8s cluster
Infrastructure (Azure MySQL, ACR, Azure k8s) should be deployed via terraform first
(a2smirnov/firsttest/terraform)

# Pipline prerequisites:
Project service connection 'ascicdacr' to ACR should be actual

Project service connection 'as-cicd-k8s' to AKS via KubeConfig (terraform output -raw kube_config) should be actual

Pipeline Secrets DB_USERNAME and DB_PASSWORD should be set

Pipeline Environment 'prod' should exist, containing Azure k8s resource with created namespace 'prod'


## Aleksei Smirnov