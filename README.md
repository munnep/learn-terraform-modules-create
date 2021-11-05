# How to use a local module

You will use a local module. This is based on the following [tutorial](https://learn.hashicorp.com/tutorials/terraform/module-create?in=terraform/modules).

In this repository you will create an AWS S3 bucket which will contain a website

# Prerequisites
Install terraform [See documentation](https://learn.hashicorp.com/tutorials/terraform/install-cli?in=terraform/aws-get-started)

Install AWS cli [See documentation](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)

# How to

## create the infrastructure
1. Clone the repository to your local machine
```
https://github.com/munnep/learn-terraform-modules-create.git
```
2. Change your directory
```
cd learn-terraform-modules-create
```
3. Give the bucket a unique name by changing the value within ```variables.tf```
```
variable "bucket_name" {
  default = "test-20210511"
}
```  
4. Terraform initialize
```
terraform init
```
5. Notice the initialize of the local module 
```
Initializing modules...
- website_s3_bucket in modules/aws-s3-static-website-bucket
```
6. Terraform plan
```
terraform plan
```
7. Terraform apply
```
terraform apply
```
8. See the website endpoint and test it in a web browser
```
website_endpoint = "test-20210511.s3-website-us-west-2.amazonaws.com"
```
9. destroy the infrastructure
```
terraform destroy
```