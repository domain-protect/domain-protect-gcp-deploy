## GCP service account creation
* log in to security tooling GCP project 
* select IAM & Admin, Service Accounts
* press Create service account
* enter a name, ID, and description for the service account

<img src="images/create-service-account.png" width="500">

* press Create and continue
* add the roles listed in [Domain Protect GCP](https://github.com/ovotech/domain-protect-gcp#deployment-permissions)

<img src="images/service-account-access.png" width="500">

* press Create
* view the newly created service account in the console

## GCP service account configuration for OIDC
* Open CloudShell
* Enter:
```
gcloud iam service-accounts add-iam-policy-binding "domain-protect-gcp-deploy@PROJECT-ID.iam.gserviceaccount.com" --member="principalSet://iam.googleapis.com/projects/PROJECT-NUMBER/locations/global/workloadIdentityPools/github-actions/attribute.repository/YOUR-GITHUB-ORG/domain-protect-gcp-deploy" --role="roles/iam.workloadIdentityUser"
```
* view in console at IAM, Service Accounts
* select Service Account, permissions

<img src="images/iam-policy-binding.png" width="700">