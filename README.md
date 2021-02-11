# GCP Terraform Docker

Project meant to create a simple docker image for use with creating infrastructure in GCP with terraform.

## Quick Start

1. Run `make`

## Usage

```bash
@docker run \
    --rm \
    -it \
    --env ENVIRONMENT=dev \
    --env TERRAFORM_DIRECTORY=/terraform \
    --env REGION=us-west1 \
    --env SERVICE_NAME=${SERVICE_NAME} \
    -v `pwd`/terraform:/terraform \
    -v $(HOME)/.gcp:/root/.gcp \
    ghcr.io/clickandobey/gcp-terraform-docker:1.0.0 \
        plan
```

The usage of this project is to produce a docker image that can be used as the basis for GCP deployments via terraform.
The dockerization makes it much easier to control the environment used between machines
