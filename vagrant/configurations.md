### Adding shell provisioner
config.vm.provision "shell", path: "setup-ng-ecosystem/setup.sh"

### Configure the box to use
config.vm.box = "ubuntu/trusty64"
config.vm.box = "bento/centos-7"

