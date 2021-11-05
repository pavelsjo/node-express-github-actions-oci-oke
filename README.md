# Github Actions setup to Deploy Node Express App in Oracle Cloud Infrastructure (OCI) - OKE

[![Deploy to OKE OCI](https://github.com/pavelsjo/node-express-github-actions-oci-oke/actions/workflows/main.yml/badge.svg?branch=main)](https://github.com/pavelsjo/node-express-github-actions-oci-oke/actions/workflows/main.yml)

This repo contains the min requeriments to deploy an `Node Express Application` in `Oracle Kubernetes Engine (OKE)` and the automation pipeline with `github actions`.

![img](./media/diagram.github-actions-oke.png)

## Setup

- Create or use an image - `Docker HUB or OCI Contanier Registry`.
  - For this example [Express App](https://hub.docker.com/r/pavelsjo/node-web-app).
- Create or use an existing [API KEY](https://youtu.be/LMvYOSkXF1k?t=271) - `OCI`.
- [Create a cluster](https://docs.oracle.com/en/learn/container_engine_kubernetes/#create-kubernetes-cluster) - `OCI`.
- Setup your [repository](https://github.com/pavelsjo/node-express-github-actions-oci-oke) and [actions](https://github.com/pavelsjo/node-express-github-actions-oci-oke/blob/main/.github/workflows/main.yml) - `Github`.
- Create [environment secrets](https://docs.github.com/es/actions/security-guides/encrypted-secrets) - `Github`.
  - **DOCKER_USERNAME**.
  - **DOCKER_PASSWORD**.
  - **OCI_USER_OCID**.
  - **OCI_FINGERPRINT**.
  - **OCI_PASSPHRASE** - [example](https://youtu.be/LMvYOSkXF1k?t=192).
  - **OCI_TENANCY_OCID**.
  - **OCI_REGION**.
  - **OKE_OCID** - [example](https://youtu.be/U4vJFUpBqNM?t=164).

## References

- Oracle
  - [CI/CD on Oracle Kubernetes Engine using Github Action](https://blog.kube-mesh.io/ci-cd-on-oracle-kubernetes-engine-using-github-action/)
  - [Adventures in CI/CD [#4]: Deploying A Microservice To The Oracle Cloud With GitHub Actions [OCI CLI Edition]](https://blogs.oracle.com/developers/post/adventures-in-cicd-4-deploying-a-microservice-to-the-oracle-cloud-with-github-actions-oci-cli-edition)
  - [Deploy Oracle Container Engine for Kubernetes](https://docs.oracle.com/en/learn/container_engine_kubernetes/#introduction)
- Node
  - [Dockerizing a Node.js web app](https://nodejs.org/en/docs/guides/nodejs-docker-webapp/)
- Docker HUb
  - [Configure GitHub Actions](https://docs.docker.com/ci-cd/github-actions/)
