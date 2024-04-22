# Demonstration of ansible-sign
To demonstrate Ansible Automation Platforms source validation features:

1. Copy the public key available in this repository, available here: [https://raw.githubusercontent.com/mglantz/ansible-secure-source-demo/main/secure-org_pubkey.asc](https://raw.githubusercontent.com/mglantz/ansible-secure-source-demo/main/secure-org_pubkey.asc)
2. Create a new set of credentials, use GPG key as type and paste in the key you copied in step 1.
3. Create a new project and define the GPG key, ensure to enable "Update revision on project launch".
4. Create an inventory with your project as source.
5. Create a job template using the playbooks/ping.yml playbook connected to the inventory you just created.
6. Run the job template. Show how the related playbook (ping.yml) now is cryptographically validated as the project is refreshed, along side with the inventory source you run against.

## How ansible-sign works with Ansible Automation Platform
Read more here: https://docs.ansible.com/automation-controller/latest/html/userguide/project-sign.html 
![How ansible-sign works](ansible-sign.png)
