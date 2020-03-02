### Install Node.js LTS, locally (not in /usr/local/bin for all users) on Centos 7 using NVM 
`sudo yum update -y`
`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash`
`nvm install --lts`

### Verify npm and node version
`node --version`
`npm --version`

### Install TypeScript tools 
`npm install -g typescript`

### Verify installation of TypeScript tools
`tsc`

### Install Bootstrap
`sudo yum install -y wget unzip`
`wget https://github.com/twbs/bootstrap/releases/download/v4.4.1/bootstrap-4.4.1-dist.zip`
`unzip bootstrap-4.4.1-dist.zip`

### Install Angular CLI
`npm install -g @angular/cli`

### Verify installation of Angular CLI
`ng`

