# using terraform to spin up AWS EC2 instance
11/23-11/24/2024
David Eliason

I am working to learn Terraform and am using the great resourc, 'Terraform: Up and Running', 3rd edition, by Y. Brikman.
The hands-on learning that I am practicing here are based on the project described in chapter two of this book.

Note: The author suggests the following for VC:
git init
git add main.tf .terraform.lock.hcl
git commit -m "Initial commit"

and to add these to .gitignore:
.terraform
*.tfstate
*.tfstate.backup

## To install Terraform on Mac:
$ brew tap hashicorp/tap
$ brew install hashicorp/tap/terraform

Allow Terraform to make changes in your AWS account with key access:
$ export AWS_ACCESS_KEY_ID=(your access key id)
$ export AWS_SECRET_ACCESS_KEY=(your secret access key)

* these env varrs apply only to the current shell, so if the computer is rebooted or a new shell is opened, these will need to be exported again

## Create a project folder and within that, a main.tf file
$ terraform init # to initialize the backend, prompt Terraform to download the code related to the provider noted in the resource provider.
