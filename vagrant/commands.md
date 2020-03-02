### Reload vagrant VMs after change to provisioners
vagrant reload --provision

### Adding shell provisioner
config.vm.provision "shell", path: "setup-ng-ecosystem/setup.sh"
