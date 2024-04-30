**Ad-hoc:**  
Ad-hoc commands in Ansible are one-liners used for quick tasks. They're executed directly from the command line without the need for a playbook. Ad-hoc commands are useful for tasks like gathering information, performing one-off changes, or troubleshooting.

**Ansible Playbook:**  
An Ansible playbook is a YAML file containing a set of tasks to be executed on remote hosts. Playbooks allow you to define complex automation workflows in a structured and reusable format. They provide more flexibility and control compared to ad-hoc commands and are suitable for managing multiple tasks or configurations.

**Inventory:**  
The inventory in Ansible is a file (typically named `inventory` or `hosts`) that contains a list of hostnames or IP addresses of the servers you want to manage. It organizes hosts into groups and allows you to define variables and group-specific configurations. Ansible uses the inventory to determine which hosts to target when executing tasks or playbooks.

**SSH Keygen Paste:**  
To paste the SSH key generated on the Ansible server to a target server, you can use the `ssh-copy-id` command. First, generate an SSH key pair on the Ansible server using `ssh-keygen`. Then, use `ssh-copy-id` to copy the public key to the target server's `authorized_keys` file. This allows you to SSH into the target server from the Ansible server without entering a password. Use the following command:

```bash
ssh-copy-id -i /path/to/your/public/key username@target_server
