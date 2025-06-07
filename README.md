# Terraform AWS Infrastructure Setup

This README provides a guide to creating a basic AWS infrastructure using Terraform. The setup includes a VPC, an Internet Gateway, a custom route table, a subnet, a security group, a network interface, an Elastic IP, and an Ubuntu server with Nginx installed.

## Steps

1. **Create VPC**: Define a Virtual Private Cloud (VPC) with a specified CIDR block.
2. **Create Internet Gateway**: Attach an Internet Gateway to the VPC to allow internet access.
3. **Create Custom Route Table**: Set up a route table and configure routes for both IPv4 and IPv6 traffic.
4. **Create a Subnet**: Define a subnet within the VPC and specify the CIDR block and availability zone.
5. **Associate Subnet with Route Table**: Associate the subnet with the custom route table created earlier.
6. **Create Security Group**: Define a security group to allow inbound traffic on ports 22 (SSH), 80 (HTTP), and 443 (HTTPS).
7. **Create Network Interface**: Create a network interface within the subnet and assign a private IP address.
8. **Assign Elastic IP**: Allocate and associate an Elastic IP address to the network interface.
9. **Create Ubuntu Server and Install Nginx**: Launch an Ubuntu instance, configure it with a network interface, and install Nginx using user data.


## Usage

1. **Initialize Terraform**: Run `terraform init` to initialize the configuration.
2. **Plan Deployment**: Use `terraform plan` to review the changes Terraform will make.
3. **Apply Configuration**: Apply the configuration with `terraform apply`.
4. **Verify Resources**: Check the outputs to find the IP addresses and instance ID.
