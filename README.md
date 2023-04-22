### Demo Project:

Ansible Integration in Terraform

### Technologies used:

Ansible, AWS, Docker, Terraform, Linux

### Project Description:

1- Create AWS EC2 Instance with Terraform

2- Write Ansible Playbook that installs necessary technologies like Docker and Docker Compose, copies docker-compose file to the server

3- Adjust Terraform configuration to execute Ansible Playbook automatically, so once Terraform provisions a server, it executes an Ansible playbook that configures the server

### Usage instruction

###### Step 1: Create AWS EC2 Instance with Terraform

1-Create a terraform.tfvars file under the root of the current folder with the following variables

```
vpc_cidr_block =
subnet_cidr_block =
availability_zone =
env_profix =
my_ip_address =
instance_type =
public_key_location  =
ssh_private_key_location =
server_user =

```

2-configure aws credentials with specified region and access_id and secret_key

```
cd ec2-instance
```

```
aws configuration
```

3-Configure vpc, ec2 instance server

###### Step 2: Create docker_deploy_app.yaml

#1 Update yum package, install python3 and docker

#2 Install docker-compose

#3 Start docker deamon

#4 Install python docker docker-compose package module

#5 Add ec2-user to docker group and reset connection

#6 Copy docker-compose.yaml file to ec2 server

#7 Docker login

#8 Start app via docker-compose

###### Step 3: Integrate ansible with terraform

![image](images/Screenshot%202023-04-21%20at%207.43.28%20pm.png)

###### Step 3: Execute the terraform

1- Initialize the Terraform project

```
terraform init
```

1- Create the VPC and EC2 instance , and configure the infrastructure: install

```
terraform apply --auto-approve
```

![image](images/Screenshot%202023-04-22%20at%2011.07.39%20am.png)

![image](images/Screenshot%202023-04-22%20at%2011.08.47%20am.png)
