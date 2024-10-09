# AWS VPC Deployment with CloudFormation and TaskCat Testing

This repository is for the NT548.P11 course - Fall 2024 semester at University of Information Technology - VNUHCM.

Provides a CloudFormation-based solution to create a Virtual Private Cloud (VPC) on AWS, complete with EC2 instances, NAT Gateway, and routing configurations. The deployment is tested using TaskCat, ensuring the infrastructure's correctness. We will also use an S3 bucket to store and deploy the CloudFormation templates.

## Table of Contents

1. [Architecture Overview](#architecture-overview)
2. [Prerequisites](#prerequisites)
3. [Folder Structure](#folder-structure)
4. [Deployment Steps](#deployment-steps)
5. [Testing with TaskCat](#testing-with-taskcat)
6. [Cleaning Up](#cleaning-up)
7. [Advantages of Using S3 for Deployment](#advantages-of-using-s3-for-deployment)

## Architecture Overview

The infrastructure deployed consists of:
- A custom VPC (`vpc.yaml`).
- EC2 instances (`EC2.yaml`).
- A NAT Gateway for outgoing internet access (`NAT.yaml`).
- Routing configuration to manage traffic within the VPC (`Routable.yaml`).

## Prerequisites

- An AWS account with the necessary IAM permissions.
- AWS CLI installed and configured.
- TaskCat installed for testing.
- CloudFormation templates stored locally or in a Git repository.
- An S3 bucket to upload and store the CloudFormation templates.

## Folder Structure

The repository contains the following files:

```plaintext
├── main.yaml          # The main CloudFormation template that includes all nested stacks
├── vpc.yaml           # VPC CloudFormation template
├── EC2.yaml           # EC2 CloudFormation template
├── NAT.yaml           # NAT Gateway CloudFormation template
├── Routable.yaml      # Routing CloudFormation template
├── taskcat.yml        # TaskCat configuration file for testing
└── README.md          # This README file
