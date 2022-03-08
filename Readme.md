# TerraForm

Understanding of Infrastructure as code

Understanding of Terraform basics and its execution flow

Understanding HCL language (Harshicorp Language System) syntax

Creating infrastructure using Terraform

Defining variables in Terraform

# SKILLS YOU WILL DEVELOP
Devops
IaC
terraform
IT Automation

# Infrastructure As Code

# Learn step-by-step
Introduction to Infrastructure as code and Terraform

Harshicorp Configuration Language syntax

Create your first infrastructure using Terraform execution flow

Updating a resource in Terraform configuration file

State file and other files created by Terraform

Defining Variables in Terraform

Passing variables via terraform.tfvars file

Writing configuration files to create a resource in Azure Cloud 

Creating a resource in Azure cloud via Terraform



# Project Overview
Terraform allows infrastructure to be expressed as code. The desired state is expressed in a simple human readable language. 
Terraform uses this language to provide an execution plan of changes, which can be reviewed for safety and then applied to make changes. 
Extensible providers allow Terraform to manage a broad range of resources, including hardware, IaaS, PaaS, and SaaS services. 

-  Introduction to Infrastructure as code 
- Terraform Harshicorp Configuration Language syntax 
-  Create your first infrastructure using Terraform execution flow 
-  Updating a resource in Terraform configuration file State file and other files created by Terraform Defining Variables in Terraform 
-  Creating a resource in Azure Cloud

# Learning Objectives
Understanding Infrastructure as code
Understanding Terraform basics and it's execution flow
Understanding HCL language (Harshicorp Language System) syntax
Creating infrastructure using Terraform
Defining variables in Terraform



# Course Objectives
In this course, we are going to focus on three learning objectives:

Understanding Infrastructure as code

Understanding Terraform basics and its execution flow

Understanding HCL language (Harshicorp Language System) syntax

Creating infrastructure using Terraform

Defining variables in Terraform

By the end of this course, you will be able to start working with Terraform (IaC) tools


# Course Structure
This course is divided into 4 parts:

Course Overview: This introductory reading material.

Terraform for absolute beginners: This is the hands-on project that we will work on in Rhyme.

Graded Quiz: This is the final assignment that you need to pass in order to finish the course successfully.


# Project Structure
The hands-on project on Course Name is divided into the following tasks:

Task 1: Introduction to Infrastructure as code and Terraform

Task 2: Harshicorp Configuration Language syntax

Task 3: Create your first infrastructure using Terraform execution flow

Task 4: Updating a resource in Terraform configuration file

Task 5: State file and other files created by Terraform

Task 6: Defining Variables in Terraform

Task 7: Passing variables via terraform.tfvars file

Task 8: Writing configuration files to create a resource in Azure Cloud 

Task 9: Creating a resource in Azure Cloud


# IAC (Infrastructure as code)

Iac is a code (human readable) that deploys your infrastructure resoruces onto various platforms instead of 
managing them manually through a user interface. Provisining infrastructure through software to achieve consistent and predictable environment.

# Wht Terraform

- No more clicks (we can write human readable code)
- Enable DevOps
- Declaritive Infrastructure
- Speed, Cost and reduce risk
- Support various private and public cloud vendors
- Idempotent
- Consistent Infrastructure

 # main.tf
resource "local_file" "games"{
         filename = "/root/rhyme/fav_games.txt"
         content = "Fifa 2021"
}


# EXECUTION FLOW

Init - > Plan - > Apply


# *terraform init*

>Initializing the backend...

>Initializing provider plugins...
  - Reusing previous version of hashicorp/local from the dependency lock file
  - Using previously-installed hashicorp/local v2.1.0

>Terraform has been successfully initialized!

> You may now begin working with Terraform. Try running "terraform plan" to see
  any changes that are required for your infrastructure. All Terraform commands
  should now work.

>If you ever set or change modules or backend configuration for Terraform,
 rerun this command to reinitialize your working directory. If you forget, other
 commands will detect it and remind you to do so if necessary.


# *terraform plan*

>Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:
   + create

>Terraform will perform the following actions:

  #local_file.games will be created
  + resource "local_file" "games" {
      + content              = "Fifa 2021"
      + directory_permission = "0777"
      + file_permission      = "0777"
      + filename             = "/root/rhyme/fav_games.txt"
      + id                   = (known after apply)
    }

>Plan: 1 to add, 0 to change, 0 to destroy.
>Note: You didn't use the -out option to save this plan, so Terraform can't guarantee to take exactly these actions if you run "terraform apply" now.




# *terraform apply*

Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:
  + create

Terraform will perform the following actions:

  #local_file.games will be created
  + resource "local_file" "games" {
      + content              = "Fifa 2021"
      + directory_permission = "0777"
      + file_permission      = "0777"
      + filename             = "/root/rhyme/terraform-labs/fav_games.txt"
      + id                   = (known after apply)
    }

Plan: 1 to add, 0 to change, 0 to destroy.

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value: yes

local_file.games: Creating...
 Error: mkdir /root/rhyme: permission denied

on main.tf line 1, in resource "local_file" "games":
 1: resource "local_file" "games"{









