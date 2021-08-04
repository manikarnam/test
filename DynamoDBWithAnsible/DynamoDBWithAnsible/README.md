AWS Services Ansible Playbook

Ansible playbook and roles for installing AWS services


Requirements:

Ansible 2.0.0 or newer

Ubuntu 16.04 (installed on your web server or virtual machine)


Instructions:

1.Clone the repository

$ git clone https://github.com/mssdevops/AWS_Ansible

$ cd /FolderName

3.Create a secret file to set your AWS access key using ansible-vault create filename
  
4.Enter Password and re-enter same password when prompted
  
5.Paste AWS access/ secret key contents in the file created as below mentioned syntax, and add any other variables as per requirement

my_access_key: **************

my_secret_key: *********************

my_region: us-east-2
  
6.Execute playbook from CLI using ansible-playbook -e @secretfilename playbook.yml --ask-vault-pass
  
7.Enter Vault password as entered during creation of secret file, then the ansible playbook execution starts from here.


Validation/ Testing:

1.Login to AWS console and make sure the required service is created as requested.

2.Make any configuration changes if necessary.
