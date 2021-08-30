# Azure DevOps pipeline test
# Push with tags containing 'Build' string triggers app deployment at azure k8s cluster
Infrastructure (Azure MySQL, ACR, Azure k8s) should be deployed via terraform first
(a2smirnov/firsttest/terraform)

# Pipline prerequisites:
Project service connection 'ascicdacr' to ACR should be actual

Project service connection 'as-cicd-k8s' to AKS via KubeConfig (terraform output -raw kube_config) should be actual

Pipeline Secret AZF_SECRET (terraform output -raw storage_account_secret) should be set for volume mounts in dev environment

Pipeline variables should be set:

ENVTYPE=dev|prod defines deployment type (dev requires porject source files upload to Azure File Share)

DB_HOST, DB_NAME (terrafrom output -raw credentials)

Pipeline Secrets DB_USERNAME and DB_PASSWORD should be set (terrafrom output -raw credentials)


## Aleksei Smirnov