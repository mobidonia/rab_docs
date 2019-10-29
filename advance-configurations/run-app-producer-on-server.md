# Run App producer on server

### Run the process NON Stop. - Server Environment <a id="run-the-process-non-stop-server-environment"></a>

The Expo CLI can work on Window, Mac, and Linux. 

So it means that you can make apps from Linux Server. 

Together with [PM2](http://pm2.keymetrics.io/) you can have a server that never stops.

With [FreshPing](https://www.freshworks.com/website-monitoring/) you can get notified when the server stops.

Let's start.



#### Create Server and Install WebMin \( Example with CentOS 7 \) <a id="create-server-and-install-webmin-example-with-centos-7"></a>

**Step1. Install Webmin  \(** [**Video**](https://youtu.be/a31MflnrvyE) **\)**

[Documentation](https://www.rosehosting.com/blog/how-to-install-webmin-on-centos-7/) on Installing WebMin.

**Step 2. Install Node, NPM, GIT, and EXPO**

1. **Install node and npm**: Read about it [here](https://tecadmin.net/install-nodejs-with-nvm/).
2. **Install GIT**: Read about it [here](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-centos-7).
3. **Install Expo**: Follow [instructions](https://docs.expo.io/versions/latest/introduction/installation/).
4. **Install PM2**: Follow [instruction](http://pm2.keymetrics.io/).
5. **Install ZIP:**  yum install zip
6. **Install UNZIP:** yum install unzip
7. **Restart Webmin** -&gt; /etc/init.d/webmin restart

To verify your installation run

* **node --version**
* **npm --version**
* **git --version**
* **expo --version**
* **pm2 --version**

**Step 3. Upload mobile app source code and install node packages**

1. **exports.isServer=true;** Change isServer to **true** in **Mobile App/Producer/config.js**
2. Via the WebMin FileManager, upload the **Mobile App** Folder \( without the **node\_modules** and **package\_lock**\)
3. Run **npm-install** in the place where it is uploaded
4. Run **expo login** and login with your account. **NOTE!!!**: This step is not recorded in the video.
5. **\[UPDATED: REQUIRED\]** You may need to run [this](https://github.com/gatsbyjs/gatsby/issues/11406#issuecomment-458769756). If you get ENOSPC: System limit for the number of file watchers  \(**REBOOT NEEDED**\)
6. Run the production script with **pm2 start ./Producer/produce.js --name AppProducer**
7. Create [Freshping.io](https://app.freshping.io/) notification. Port **8989**

\*\*\*\*[**VIDEO DOCUMENTATION HERE**](https://www.youtube.com/watch?v=ilP6l7K7YzA)\*\*\*\*

\*\*\*\*



