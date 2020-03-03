### Look up doc for an ansible module
ansible-doc -s lineinfile  

### Look up doc for an ansible module (more verbose)
ansible-doc lineinfile 

### List all installed Ansible modules
ansible-doc -l

### Ansible module to view all facts as gathered from a host by Ansible
ansible myhost1 -m setup

### Ansible module to verify if a host (or group of hosts) is reachable
ansible myhost1 -m ping  

### Ansible module to install software (redhat based). Grab the latest version of httpd in the repo
ansible myhost1 -m yum -a "name=httpd state=latest"

### Ansible is not going to use sudo privilege escalation unless we tell it to. So how do we mitigate that?
ansible myhost1 -b -m yum -a "name=httpd state=latest"

### Ansible module to control daemons (for eg. the httpd service)
ansible myhost1 -b -m service -a "name=httpd state=started"

### command to run Ansible playbooks
ansible-playbook  

### command to run Ansible playbook with a specific inventory file
ansible-playbook -i myinv my_playbook.yml  

### Pass variables via CLI while running a playbook called service.yml
ansible-playbook my_playbook.yml -e "target_hosts=localhost target_service=httpd"  

### Referencing Ansible the variables target_hosts & target_service in a playbook
hosts: "{{ target_hosts }}"  
yum:  name="{{ target_service }}"  

### Dry run ansible playbook for sanity check
ansible-playbook my_playbook.yml --check  

### To retry playbook for hosts where the tasks failed, which file is generated?
my_playbook.retry  
Use in conjunction with "--limit"  

TO DO example  
