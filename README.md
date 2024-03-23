# Ansible Project

This project contains documentation and files for managing infrastructure using Ansible.

## Getting Started

Follow these instructions to set up your Ansible environment and run playbooks.

### Prerequisites

Make sure you have the following prerequisites installed on your local machine:

- Ansible
- SSH client

### Steps

1. **Create SSH Key**: Generate an SSH key pair using the following command:
   ```bash
   ssh-keygen -t rsa
    ```
2. **Copy SSH Key to Host Machine**: Use ssh-copy-id to copy the public key to the remote host:
   ```bash
   ssh-copy-id username@ip
     ```
3. **Create an Inventory File**: Create an inventory:
    ```yaml
    all:
 	 hosts:
   		 ip_address:
    			 ansible_user: username
     ```
4. **Test Ping**: Use Qnsible to test ping connectivity to qll hosts in the inventory:
     ```bash
     ansible -i inventory.yaml all -m ping
     ```
5. **Create Playbook**  Create a playbook file named playbook.yaml where you define the tasks to be executed.
    ```bash
    vim playbook.yaml
    ```
6. **Run Ansible Playbook**  Execute the Ansible playbook using the inventory file:
 	```bash
 	ansible-playbook -i inventory.yaml playbook.yaml
	 ```

