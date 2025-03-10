# 4640-w9-lab-start-w25

Marcus Su, Rafeel Geelani, Tuan Nguyen


make a new ssh key

```
ssh-keygen -t ed25519 -f ~/.ssh/lab9 -C "key for lab 9"
```
import to aws
```
./import_lab_key  ~/.ssh/lab9.pub
```
 Initializes Packer
```
packer init .
```
Formats the ansible-web.pkr.hcl

```
packer fmt ansible-web.pkr.hcl
```
Checks that ansible-web.pkr.hcl has the right syntax
(Make sure to do "." instead of ansible-web.pkr.hcl)
This makes it so that all the files in the current directory
are referenced
```
packer validate .
```
Builds the machine image
(Make sure to do "." instead of ansible-web.pkr.hcl)
```
packer build .
```
You should now have an AMI in your AWS account

Initializes a Terraform working directory
```
terraform init
```
Validates the syntax and configuration of the Terraform file
```
terraform validate
```
Generate an execution plan 
```
terraform plan
```
Applies the Terraform configuration
```
terraform apply
```
You should now have an instance running from the AMI
