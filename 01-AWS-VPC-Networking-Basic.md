AWS VPC Networking Basics

This project demonstrates a basic setup of an AWS Virtual Private Cloud (VPC) to host a web application, covering network fundamentals like public and private subnets, availability zones, and internet gateway routing.
Project Overview

The setup includes:

    A single VPC with a CIDR block of 10.0.0.0/16.
    Two public subnets (in different availability zones) for web servers or external services.
    Two private subnets (in the same availability zones) for internal services, isolated from direct internet access.
    An internet gateway and routing configurations to allow internet access only for public subnets.
![1](https://github.com/user-attachments/assets/048f84fd-2d6a-4f09-8d38-6073c22b5dc1)



Requirements

The requirements were:

    VPC with CIDR block 10.0.0.0/16
    2 Public Subnets in separate availability zones:
        10.0.10.0/24 (AZ A)
        10.0.20.0/24 (AZ B)
    2 Private Subnets in the same availability zones as above:
        10.0.100.0/24 (AZ A)
        10.0.200.0/24 (AZ B)
    Routing and Internet Access:
        Only the public subnets have internet access through an Internet Gateway.
