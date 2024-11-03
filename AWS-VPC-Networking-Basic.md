![1](https://github.com/user-attachments/assets/d43b8431-e258-40c5-afb6-b8865887cbc7)

Project Overview

The setup includes:

    A single VPC with a CIDR block of 10.0.0.0/16.
    Two public subnets (in different availability zones) for web servers or external services.
    Two private subnets (in the same availability zones) for internal services, isolated from direct internet access.
    An internet gateway and routing configurations to allow internet access only for public subnets.

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
