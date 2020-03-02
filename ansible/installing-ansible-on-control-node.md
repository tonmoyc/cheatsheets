## Installing Ansible using python pip

### Creating a non-root user on controller called ansible
sudo useradd ansible
sudo passwd ansible
echo "ansible ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers.d/ansible
su - ansible

### Installing 
sudo yum update -y
sudo yum install -y python3 python3-pip
alternatives --set python /usr/bin/python3
su - ansible
pip3 install ansible --user
ansible --version
