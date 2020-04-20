# Run App producer on server

### Run the process NON Stop. - Server Environment <a id="run-the-process-non-stop-server-environment"></a>

The Expo CLI can work on Window, Mac, and Linux. 

So it means that you can make apps from Linux Server. 

Together with [PM2](http://pm2.keymetrics.io/) you can have a server that never stops.

Let's start.



#### Create Server  \( Example with CentOS 7 \) <a id="create-server-and-install-webmin-example-with-centos-7"></a>

**Step 1. Install Node, NPM, GIT, and EXPO**

1. **Install node and npm**: Read about it [here](https://tecadmin.net/install-nodejs-with-nvm/).
2. **Install GIT**: Read about it [here](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-centos-7).
3. **Install Expo**: Follow [instructions](https://docs.expo.io/versions/latest/introduction/installation/).
4. **Install PM2**: Follow [instruction](http://pm2.keymetrics.io/).
5. Install mexpo-cli with the command `npm i -g mexpo-cli`
6. To make your VPS handle more operations  - Restart after that `echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p`  

Full list of command

```text
yum -y update

clear

curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash                        
                                                                                                      
source ~/.bashrc                                                                                      
                                                                                                      
nvm install v12.14.1                                                                                  
                                                                                                      
npm install -g --unsafe-perm --verbose expo-cli        

npm install -g --unsafe-perm --verbose firebase-tools
                                                                                                      
npm install pm2 -g    

yum -y install git
                                                                                                      
npm install -g --unsafe-perm --verbose mexpo-cli

echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p

source ~/.bashrc   
```

To verify your installation run

* **node --version**
* **npm --version**
* **git --version**
* **expo --version**
* **pm2 --version**
* **mexpo-cli --version**

**Step 2. Upload mobile app source code and install node packages**

1. Make sure you have configured Mobile App/Producer/config.js with your own data. Email, smtp etc.
2. You should have also followed and completed the steps for the Local App producer. We need modified firebase\_config.js file and services\_account json file. 
3. You will need to upload the code on some GIT platform like GitLab, GitHub or BitBucket. Initialize your local Mobile App folder.
4. Connect via SSH to your VPS
5. Clone the code from your repository.
6. Go inside your cloned code
7. Run **`npm install`** 
8. Run **`expo login`** and login with your account.



Now. Run the production script with **`npm run pmserver`**

The server producer is now up and running. 

