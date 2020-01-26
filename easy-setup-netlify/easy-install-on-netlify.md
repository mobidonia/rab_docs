---
description: Netlify offer continues deployment for our App Builder
---

# Easy install on netlify

## Become our collaborator on Github

By  becoming our collaborator, you will always have access to the latest code. [Send us](https://help.mobidonia.com/#reactappbuilder) your GitHub username and purchase code. 

Then we will add you as collaborator on our repository.

[Fork it. ](https://help.github.com/en/github/getting-started-with-github/fork-a-repo)

Then you will have your own clone of the App Builder site. You can easily sync the changes from our source code.

{% hint style="info" %}
If you don't want to wait for us to give you access, you can [create new private repository with the code](https://www.softwarelab.it/2018/10/12/adding-an-existing-project-to-github-using-the-command-line/) you downloaded from Code Canyon \(Builder Folder\). But this way you lose the opportunity to sync with our source code when we release new version. 
{% endhint %}

## Create Firebase Database

Instructions here

{% page-ref page="../requirements/setup-project-config-file/firebase-account-setup.md" %}

## Publish on Netlify

[Create account on Netlify.](https://www.netlify.com/)

Click on the button "New GIT Site" 

Then select Github and connect with your account where you have forked the repository. 

For **Build command** enter: `node fillenv.js && npm run build:cloud`

**Environment variables**

{% hint style="success" %}
* [ ] REACT\_APP\_appName              - Your Project name
* [ ] REACT\_APP\_isSaaS                    - true
* [ ] REACT\_APP\_adminEmail           - your desired admin email
{% endhint %}

{% hint style="success" %}
* [ ] REACT\_APP\_apiKey                    - Firebase Api Key \( from console.firebase.com \)
* [ ] REACT\_APP\_appId                      - Firebase App ID \( from console.firebase.com
* [ ] REACT\_APP\_projectId                - Firebase Project ID \( from console.firebase.com \)
{% endhint %}

{% hint style="success" %}
* [ ] REACT\_APP\_privateKey             - Private key \( from service account json \)
* [ ] REACT\_APP\_serviceAccount . - client\_email \( from service account json \)
{% endhint %}

To download service account JSON file go in  console.firebase.com then in Project -&gt; Project Settings - &gt; Service Accounts and click on "**Generate new private key**"

Now on Netlify, click on "**Deploy new site**". 



