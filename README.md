# AWS Certified Cloud Practitioner - Notes
Repositório de anotações para estudo da prova AWS Certified Cloud Practitioner.

## Introduction

Problems Solved by Cloud

* Flexibility
* Cost-Effectiviness
* Scalability
* Elasticity
* High Availability and Fault-Tolerance
* Agility

## Pricing

* Compute</br>
    * Pay for computing time

* Storage</br>
    * Pay for data stored in the Cloud

* Data transfer OUT of the Cloud:</br>
    * Data transfer in is free
    
Only Manage application and Data (PaaS)

Which Global Infrastructure is composed of one or more discrete data centers with redundant power, nertworking, and connectiviy and are used to deploy infrastructure

Multi-Tenancy and resource pooling is one of five characteristics of cloud computng, supports multi-tenant model and multiple customers are services from the same physical resources

Five Characteristics of Cloud Computing

On-Demand self service
Multi-tenancy  and resource pooling
Broad network access
Rapid elasticity and scalability
Measured Service

Four points when choosing an AWS Region are:
Compliance with data governance and legal requirements
proximity to customers
available services and features within a Region
pricing

Cloud Computing def: On-demand availability of computer system resources, especially data storage (cloud storage) and computing power, without direct active management by the user

Elaticity def: Automatic and quick ability to acquire resources as you need them and relear resources when you no longer need them


------------------------------------------------------------------------------------

IAM - Identity and Access Managemente, Global Service
root account
users
groups only contains users, not groups

IAM: Permissions
users or groups can be assigned json documents called policies
least privilege principle: dont give more permissions than a user needs

IAM Policies Structure
   Version
   ID
   Statmente

IAM Password Policiers
    variable and different password types
  or
   MFA   - Multi Factor Authentication
    MFA = password you know + security device you own (token)
    
    Virtual MFA device (google authentication and Authy)
   
   IAM Roles for Services
   IAM Role will be just like a user, but instead they will be used by aws services
   EC2 Instance Roles
   Lambda Functions Roles
   Roles for CloudFormation
   
   IAM Securyti Tools
      IAM  Credentials Report (account-level)
      IAM  Access Advior (userlever)
      
 Shared Responsability Model for IAM
 
 AWS
 Infrastructure (global network security)
 Configuration and vulnerability analys
 Compliance validation
 
 You
 Users, Groups, Roles, POlicies management and monitoring
 Enable MFA 
 Rotate your keys
 Use IAM 
 Analsyse patterns
 -----------------------------------------------------
 Amazon EC2
   EC2 = Elastic Cloud Computing
      Renting virtual machine - EC2
      Storing Data on virtual drivers - EBS
      Distribuiting load across machine - ELB
      Scaling the services using an auto-scaling group - ASG
