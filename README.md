# Salesforce

This repository contains the source code and configurations for our Salesforce project, along with GitHub actions for automating the deployment process.

## Prerequisite

To work with this project you shoud have installed:

1. VSCode with extenstions: *Salesforce CLI Integration* and *Salesforce Extension Pack*
2. Git

## How to start coding

Clone Git project: git clone https://github.com/SasaGavric/salesforce-cicd.git

### Before you start coding

Before you start working on your branch you need to have your *Dev Env (Developer Edition Sandbox)* synchronized with your branch. To achive this you need to deploy all code to the Org *(steps for VSCode)*:

1. Authorize an Org: `[Cmd + Shift + P]` and type `SFDX: Authorize an Org`
2. Deploy source to Org: Right click on force-app in the project and from dropdown menu click `Deploy source to Org`


## Branching Model and GitHub Actions

#### Branches
- **master** - Production Sandbox
- **dev** - Dev Sandbox
- **feature/** - development
- **bugfix/** - bug fix
- **release/** - release
- **hotfix/** - hotfix in production


#### GitHub Actions
- Create ***Pull Request*** on *feature/* or *bugfix/* branch triggers Validate Deploy to Dev Sandbox
- Create ***Pull Request*** on *release/* branch triggers Validate Deploy to Production
- Merge *feature/* or *bugfix/* triggers Deploy or \*Quick Deploy to Dev Sandbox (1 approval needed)
- Merge *release/* or *hotfix/* triggers Deploy or \*Quick Deploy to Production (2 approval needed)

## Read All About It
- [Salesforce Extensions Documentation](https://developer.salesforce.com/tools/vscode/)
- [Salesforce CLI Setup Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_intro.htm)
- [Salesforce DX Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_intro.htm)
- [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference.htm)
