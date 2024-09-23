# vim main.tf
        terraform {
  required_providers {
    aws = {
      source = "hashicorp/aws"
      version = "5.67.0"
    }
  }
}

provider "aws" {
        region     = "us-east-1"
}

variable "envi" {
        description = "Enter dev or prod"
        type        = string
}

resource "aws_instance" "myinstance" {
        ami = "ami-0ebfd941bbafe70c6"
        instance_type = var.envi == "prod" ? "t2.small" : "t2.micro"
        tags = {
                Name = "condition_example"
}
}
