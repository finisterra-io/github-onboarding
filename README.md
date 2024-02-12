# github-onboarding

This repository contains several workflows for managing Terraform infrastructure.

## AWS Auth

Create a role in aws called gha-cicd using the following cloudformation [template](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/review?templateURL=https://s3.amazonaws.com/finisterra-aws-connect/finisterra-gh-role.yaml&stackName=finisterra-gh-role&param_GitRepositoryOwner=ORG_NAME), this role only grants permissions from your github organization to AWS.

## Finisterra API token secret

You need to crete a Github secret called `GITHUB_TOKEN` with the finisterra api token. That can be obtained from https://app.finisterra.io

## Workflows

### Apply Terragrunt

This workflow applies Terragrunt configurations. You can find the workflow in the [apply_terragrunt.yaml](apply_terragrunt.yaml) file.

### Generate Terraform Code1

This workflow generates Terraform code. You can find the workflow in the [generate_tf_code.yaml](generate_tf_code.yaml) file.

Before using the workflow replace the `<AWS_ACCOUNT_ID>`, and `<AWS_REGION>` with your relevant values

### Plan Terragrunt

This workflow plans Terragrunt configurations. You can find the workflow in the [plan_terragrunt.yaml](plan_terragrunt.yaml) file.

## License

This project is licensed under the terms of the license found in the [LICENSE](LICENSE) file.
