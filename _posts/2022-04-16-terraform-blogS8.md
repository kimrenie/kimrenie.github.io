---
layout: post
title:  "S8. Terraform"
date:   2022-04-16 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 75%}</style></html>

# Terraform Basics

![image](/images/terraform.jpg)

Terraform is an open-source software that was created by Hashicorp in order for developers to acccess and create "infrastruture as code." The utilization of "infrastructure as code" enables the usage of declaritive coding language in order to build (or later edit and change) a company's Information Technology resources and infrastructure. A plan is created after running the original script and is later executed to provision all of the resouces properly.

The added utility given to us by Terraform allows this process to become more automated with less things to manage and handle manually. Some of the benefits that Terraform gives us are: speeding up the test and development times, maintaining original environemnt and this improving overall consistency, etc.

> The four commands that are essential to properly utilize Terraform are as follows:

```
$ terraform init
$ terraform plan
$ terraform apply
$ terraform destroy
```
Terraform init is used in order to initilaize the working environment. 
Terraform plan is used in order to lay out the actions that are intended to happen against the current environment. This stage can also be understood as the trial run and will catch possible errors before the user is able to apply and incorrect changes during the apply phase. 
Terraform apply is used in order to execute the prior plan and create our resources. 
Terraform destroy is used in order to get rid of this environent and the resources that were created with it. 

# Terraform Configuration Files

A configuration file (*.tf or main.tf) is created by the user in order to identify the provider that will be used alongside specifics about resources. 

A file containing variable declarations (variables.tf) is used to declare variables that will be used to set up our resources. 

A variable definition file (terraform.tfvars) contains the values associated to our input variables. 

Lastly, a state file (terraform.tfstate) is automaticaly created alongside a terraform apply and contains the state of the created infrastructure. 

# Resources 

https://www.ibm.com/cloud/learn/terraform
https://www.ibm.com/cloud/learn/infrastructure-as-code
https://k21academy.com/terraform-iac/terraform-beginners-guide/