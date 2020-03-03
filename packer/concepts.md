Packer has templates that are json files.  
What are the Template components?  

- builder: Is this going to be an image for AWS, or a Docker image?  
- description: Description of the machine image  
- min_packer_version: version of Packer used  
- post-processors: What actions to perform after the machine image has been created, such as tagging the image, publishing a Docker image to a repo.  
- provisioners: How we are going to provision our machine images? (ansible, chef, puppet, script)  
- variables: key-value pairs that will be used in our templates  

Commonly supported Packer Builders:-  
- Amazon AMI
- Azure Resource Manager
- Docker
- HyperV
- OpenStack
- VirtualBox
- VMWare

Commonly supported Provisioners:-
- Ansible: Local (Ansible will be installed on guest machine, and the playbooks uploaded and executed)
- Ansible: Remote (Running Ansible in the traditional way, where an Ansible control node will SSH into the guest and provision)
- Chef
- File: Upload a file, tar, or folder that will provision
- PowerShell: For Windows machine images
- Puppet: First shell provisioner needs to install Puppet agent on the guest machine
- Shell: shell commands(inline method) or shell scripts

Commonly used Post Processors:-  
- Amazon Import: This will upload your OVA artifact to AWS and create an AMI out of it
- Checksum: Create a checksum for the artifact that can be used to verify its integrity later
- Docker Push: push to remote Repository
- Docker Tag: Tag a container image
- Shell
- vSphere
- Vagrant
