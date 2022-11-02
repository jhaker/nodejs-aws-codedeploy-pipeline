# nodejs-aws-codedeploy-pipeline

### ssh to linux to install packages 
 ssh -i "teachandshare.pem" ec2-user@ec2-34-238-151-122.compute-1.amazonaws.com -v
 or
 ssh -i "teachandshare.pem" ec2-user@34.238.151.122 -v
 
### update and upgrade linux machine and install node, nvm, pm2 
sudo yum install deltarpm
sudo yum update 
sudo yum upgrade 
sudo yum install -y git htop wget 

To **install** or **update** nvm, you should run the [install script][2]. To do that, you may either download and run the script manually, or use the following cURL or Wget command:
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
```
```sh
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash

https://github.com/nvm-sh/nvm/blob/master/README.md


```sh
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion" # This loads nvm bash_completion
```

```sh
nvm --version 
```

```sh
nvm install 16
nvm install --lts #latest stable node js server version
```

```sh
nvm --version
```

```sh
npm -v
```
