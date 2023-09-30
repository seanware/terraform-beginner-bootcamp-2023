# Terraform Beginner Bootcamp 2023

- [Semantic Versioning](#semantic-versioning-mage)
- [Git](#install-the-git-log-graph-extension)
- [Terraform CLI](#fixed-terraform-cli-installation)
- [Environment Variables](#terraform-env-variables)
- [AWS CLI Refactor](#aws-cli-refactor)
- [Terraform Random Provier](#implement-the-terraform-random-provider)
- [Install AWS provider](#tested-terraform-with-aws)

## Semantic Versioning :mage:

This project uses the  established conventions for semantic versioning for its tagging which are listed below.
[semver.org](https://semver.org/)

Given a version number **MAJOR.MINOR.PATCH**, increment the

   1. **MAJOR** version when you make incompatible API changes
   2. **MINOR** version when you add functionality in a backward compatible manner
   3. **PATCH** version when you make backward compatible bug fixes

Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

## Install the git-log graph extension

To better visulize the git workflow I have installed the free git-log graph tool
[git_log_graph](https://github.com/phil294/git-log--graph#readme)

## Fixed Terraform CLI installation
security keys
The terraform cli installation commands were out of date and need to update with new gpg keyring.
[Installation Instrutions](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli) 

Further, the terraform cli installation was automated using a [bash script](./bin/install_terraform_cli) located at /bin/install_terraform_cli and modification were made to the [gitpod.yml](/.gitpod.yml) file so a script could be used.
[Gitpod Documentation](https://www.gitpod.io/docs/configure/workspaces/tasks#prebuild-and-new-workspaces)

## Terraform env variables

Environment variables were added to the terrafrom script and stored in the gitpod workspace for longterm usage
[Gitpod env Documentation](https://www.gitpod.io/docs/configure/projects/environment-variables#ways-of-setting-user-specific-environment-variables)

## AWS CLI refactor

The access keys for the aws cli were created using the aws management console an stored as environment variables and loaded into gitpod.
[AWS env variables](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-envvars.html)

## Implement the terraform random provider

The terraform random provider was implemeted to determine if the basic commands were completely functional.  The link to the provier documentation is located here: [Random provider](https://registry.terraform.io/providers/hashicorp/random/latest/docs)

The terraform.lock.hcl file should be included in the repository as it is unique to each terraform plan. [Terraform lock file](https://developer.hashicorp.com/terraform/language/files/dependency-lock#lock-file-location)

## Tested Terraform with AWS

The aws provider was installed from the terraform resgistry [AWS provider link](https://registry.terraform.io/providers/hashicorp/aws/latest/docs) with the provider a S3 bucket was created and destroyed using terraform plan, apply and destory.  The link the the aws S3 resoure documentation is here: [S3 resource](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket)