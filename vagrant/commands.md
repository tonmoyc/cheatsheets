### Most basic commands in Vagrant

vagrant init: Initialize the current directory to be a Vagrant environment by creating a Vagrantfile
vagrant validate: Validate a custom Vagrantfile
vagrant up: Create & configure guest VMs as defined in the Vagrantfile
vagrant halt: Stop the VMs(as defined in the Vagrantfile) that are up and running
vagrant destroy: Destroy and release resources(disks) being used by the guest VMs
vagrant reload: Used after making changes to the Vagrantfile, since we want those changes to reflect in our guest VMs
vagrant ssh: SSH into a specific guest VM
vagrant status: show state of the guest VMs
vagrant provision: Run any software provisioners (shell scripts, ansible, puppet, chef) configured in the Vagrantfile, manually. Usually these scripts run only once, the first time the guest VM starts up.

### Reload vagrant VMs after change to provisioners
vagrant reload --provision

### Adding shell provisioner
config.vm.provision "shell", path: "setup-ng-ecosystem/setup.sh"
