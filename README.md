# Terraform Beginner Bootcamp 2023

- [Semantic Versioning](#semantic-versioning-mage)
- [Git](#install-the-git-log-graph-extension)
- [Terraform CLI](#fixed-terraform-cli-installation)
- [Environment Variables](#terraform-env-variables)

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