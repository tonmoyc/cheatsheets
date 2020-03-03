### Where is the default ansible.cfg stored?
/etc/ansible/ansible.cfg  

### Where is the default inventory file stored?
/etc/ansible/hosts  

### Example of group of hosts
[webservers]  
alpha.example.com  
green.example.com  
192.168.8.10  

### Patterns to define hosts
www[001:006].example.com  

### Setting up an alias to an inventory host
alphasrv ansible_host=alpha.example.com  
greensrv ansible_host=green.example.com  

