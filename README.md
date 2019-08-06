# Introduction 
This Module will create a Resource Group in Azure 

# Provision Instructions

Copy and paste into your Terraform configuration, insert the variables, and run terraform init, terraform, plan and terraform apply : 


module "resource-group" {
  source  = "git::https://DickiesInfrastructure@dev.azure.com/DickiesInfrastructure/WD-Terraform-Modules/_git/TF-AZ-Resource-Group"
  # insert the 3 required variables here
  Location = "Location"
  Name = "Name"
  Tags = {
      tag1 = "value1"
      tag2 = "Value2"
  }
  }




# Example:

module "resource-group" {
  source  = "git::https://DickiesInfrastructure@dev.azure.com/DickiesInfrastructure/WD-Terraform-Modules/_git/TF-AZ-Resource-Group"
  Location = "south central us"
  Name = "JO-Test-RG"
  Tags = {
  source  = "adfinis-forks/resource-group/azurerm"
  location = "south central us"
  name = "JO-Test-RG"
  tags = {
      Department = "IT"
      Owner = "JO"
  }
  }