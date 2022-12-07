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

```sh
cd /home/ec2-user
```

```sh
git clone https://github.com/jhaker/nodejs-aws-codedeploy-pipeline.git
```

cd nodejs-aws-codedeploy-pipeline
npm i
node app.js # test http://34.238.151.122:3000/
npm install -g pm2


### set node, pm2 and npm available to root user
sudo ln -s "$(which node)" /sbin/node 

sudo ln -s "$(which npm)" /sbin/npm 

sudo ln -s "$(which pm2)" /sbin/pm2  


### starting th eapp as sudo(run nodejs in the background and when the server starts)
sudo pm2 start app.js --name=nodejs-express-app 

sudo pm2 save # saves the running process, if not saved, pm2 will forget the running apps on next boot 

### impotant if you want pm2 to start on system boot 
sudo pm2 startup # starts pm2 on computer boot 


### install aws code deploy agent
sudo yum install -y ruby


wget https://bucket-name.s3.region-identifier.amazonaws.com/latest/install




