# HW1
This repository contains the code for implementing Homework1 requirements of DevOps (CSC519) in Fall 2017.

## Ansible Scripts

1. main.yml:https://github.ncsu.edu/manush/HW1/blob/master/main.yml

2. Inventory:https://github.ncsu.edu/manush/HW1/blob/master/inventory


## Screencasts: 

The link to access the Screencast is: https://www.youtube.com/watch?v=nf_X94e0fP0


### Instructions for Running the ansible scripts:

1. Created Vagrant node-host machines. One being ansible server and another as node.
2. Ensure that the server can ping the host. The Host to be configured should have access to internet.
3. Also Ensure that the private key of the node is present in the ansible server.
4. To modify the hostname, password, directory of the vagrant VM or the image to boot the vagrant VM, please edit the variables remote_username, remote_password,  remote_image or remote_dir respectively in the main.yml file.
4. Run ansible playbook yaml file. Ansible playbook file is main.yml

Sample connectivity:
![Alt text](sample_topology.png?raw=true "Sample Topology for ansible and remote node")

The command to run the playbook is: "ansible-playbook -i inventory main.yml -s"
This file will

(1) Install Python2 on the Ubuntu 16.04 VM that is referenced in the inventory file.

(2) Install Dependencies for VirtualBox, phpVirtualBox, Vagrant.

(3) Configure the VM for phpVirtualBox, VirtualBox.

(4) Starts the vboxweb-service, vboxdrv and apache2 service for phpVirtualBox.

(5) It also creates a Vagrant VM.

3. For verification of vagrant, we can now ssh into the node VM and check the status of the Nested VM created in Step 4-(5).
4. For verification of phpVirtualBox, on the browser we can go to http://node_IP/phpvirtualbox.

