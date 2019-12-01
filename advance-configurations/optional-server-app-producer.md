---
description: >-
  Note that this step is not required. You can tun you app producer locally
  only.
---

# \[Optional\] Server App producer

## Why and when I need a Server App producer

You will need server app producer if you have more than 10 apps for you or you clients. And you need automated app making

{% hint style="info" %}
 We will first recommend to do a test app and compile it with local producer.
{% endhint %}

Once you have tested the local producer,  you can follow this guide to setup your server.

## Initialize your VPS

Get a Linux VPS. 2GB+ of RAM. Cheapest option is [Time4VPS](https://www.time4vps.com/?affid=3906) \( Choose Linux VPS \).  Install Cent OS 7.

* Login via **ssh**
* **Install** _**node**_ **and** _**npm**_. Full guide [here](https://tecadmin.net/install-nodejs-with-nvm/).

```text
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
source ~/.bashrc
nvm install v12.9.0
source ~/.bashrc
node --version
```

* **Install** _**Expo**_: Full [instructions](https://docs.expo.io/versions/latest/introduction/installation/).

```text
npm install -g expo-cli
source ~/.bashrc
expo --version
expo login
```

* **Install** _**PM2**_: Full [instructions](http://pm2.keymetrics.io/).

```text
npm install pm2 -g
```

