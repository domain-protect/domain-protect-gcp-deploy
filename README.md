# domain-protect-gcp-deploy
Deploy Domain Protect for GCP

Deploy [Domain Protect GCP](https://github.com/ovotech/domain-protect-gcp) using GitHub Actions

* Deploy Domain Protect in your GCP environment
* No need to clone or fork Domain Protect GCP
* Internal / private deployment repository to protect sensitive information
* Uses OpenID Connect - GCP service account keys not needed
* Update to latest version of Domain Protect GCP any time by running pipeline

## pipeline steps
Pipeline triggered manually and also on `git push` of the main branch

* Terraform plan and apply of Domain Protect GCP dev in security tooling account
* Terraform plan for Domain Protect GCP prd in security tooling account (approval required)
* Terraform apply for Domain Protect GCP prd in security tooling account (approval required)

# before starting
* check [requirements](https://github.com/ovotech/domain-protect-gcp)

## how to set up
* [Configure GCP Workload Identity and pool](docs/WORKLOAD.md)
* [Configure GCP Service Account](docs/SERVICE.md)
* [Create and configure deployment repository](docs/REPO.md)
* [Deploy using GitHub Actions](docs/DEPLOY.md)

## keep up to date with Domain Protect GCP
* create a custom watch on Domain Protect GCP repository
* when notified of a new release, run your GitHub Actions pipeline