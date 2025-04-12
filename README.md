# acr-aks-pipeline



✅ Steps to Deploy Dockerized HTML App to AKS Using Azure DevOps

Created a Dockerfile for the HTML app inside the app/ folder.

Pushed the project to an Azure DevOps repository.

Created a service connection in Azure DevOps for:

Azure Container Registry (ACR)

Azure Kubernetes Service (AKS)

Wrote a CI pipeline (app-ci-pipeline.yml) to:

Build a Docker image.

Tag it with Build.BuildId.

Push it to ACR.

Publish Kubernetes manifests as artifacts.

Wrote a CD pipeline (app-cd-pipeline.yml) to:

Download the published manifests.

Replace the container image dynamically with the new build.

Deploy the updated app to AKS using KubernetesManifest@1.

Configured Kubernetes deployment and service manifests to run the app in AKS and expose it via a LoadBalancer.

Triggered the CI pipeline by pushing changes to the app folder.

Automatically triggered the CD pipeline after successful CI.

Verified the deployment by checking the AKS service’s external IP and accessing the app in a browser.
