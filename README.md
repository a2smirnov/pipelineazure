# Azure DevOps pipeline test
# Push triggers app deployment at azure k8s cluster
Infrastructure (Azure MySQL, ACR, Azure k8s) should by deployed via terraform first
(a2smirnov/firsttest/terraform)

# Pipline prerequisites:
### Secrets DB_USERNAME and DB_PASSWORD should be set
### Environment 'prod' should exist, containing Azure k8s resource with created namespace 'azure-pipeline'
### Project service connection 'ascicdacr' to ACR should exist
### Project service connection 'as-cicd-k8s' to AKS via KubeConfig should exist

## Aleksei Smirnov