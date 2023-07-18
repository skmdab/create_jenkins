# Create Jenkins

This repository contains scripts and configurations to deployment of Jenkins Instance on AWS.

## Prerequisites

Before you can use these scripts, ensure that you have the following:

- Linux or macOS environment
- AWSCLI installed and configured with crredentials
- Docker & Jenknins installed and running
- Git installed
- Ansible installed and running
- Internet connectivity to download Jenkins Docker image
- Jenkins user must be part of Docker group


Modify VPC, AZ, Security groups, AMI Id, Subnets & PEM file name in aws_create script according to yours.

## Create Jenkins Job with pipeline and choose Pipeline Script from SCM.

To Do's in Jenkins
------------------------------------------
Add AWS pem file in jenkins credentials with ID "pemfile"
