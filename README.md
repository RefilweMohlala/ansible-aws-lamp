# ansible-aws-lamp
Automated LAMP Stack Deployment with Ansible on AWS EC2

## Overview
This project demonstrates how to use Ansible to automate the process of setting up a LAMP stack on an AWS EC2 instance. It involves provisioning the EC2 instance, installing Apache, MySQL, and PHP, and deploying a simple PHP-based website.

## Prerequisites
Before running the playbook, ensure you have the following:

AWS Account: You’ll need access to an AWS account to create EC2 instances.
AWS CLI: Installed and configured with your AWS credentials.
Ansible: Installed on your local machine or master server.
SSH Key: Ensure you have your SSH key for authenticating with your AWS EC2 instance.

## Getting Started
1. ## Set Up Your AWS EC2 Instance
Go to your AWS Management Console and create an EC2 instance (Ubuntu recommended).
Make sure the instance has the necessary security group settings to allow SSH (port 22) and HTTP (port 80) access.
Obtain the public IP of the EC2 instance.
2. ## Configure Ansible

- Clone this repository to your local machine or master node:
 `git clone https://github.com/RefilweMohlala/ansible-aws-lamp.git`
- Navigate to the project directory:
  `cd ansible-aws-lamp`
- Edit the inventory.ini file to include the public IP of your EC2 instance:
  `[lamp]
<your-ec2-public-ip>`
-Update the lamp_playbook.yml if needed, such as configuring custom variables for the website or MySQL.

# Usage
## Running the Playbook
Ensure that you have SSH access to your EC2 instance.
Run the Ansible playbook to set up the LAMP stack on your EC2 instance:
`ansible-playbook -i inventory.ini lamp_playbook.yml`

## This command will:

- Install Apache, MySQL, and PHP.
- Deploy a basic PHP site to the /var/www/html directory.
- Ensure that Apache and MySQL are running and the website is accessible.

# Project Structure
 `ansible-aws-lamp/
│
├── lamp_playbook.yml       # Main Ansible playbook to set up the LAMP stack
├── inventory.ini           # Ansible inventory file with EC2 instance details
├── README.md               # This file
├── index.php               # Simple PHP website file
├── ansible.cfg             # Optional Ansible configuration file`



 
