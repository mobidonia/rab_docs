---
description: Netlify offer continues deployment for our App Builder - For free.
---

# Easy install on Netlify

## Make Firebase and Paddle Account

{% page-ref page="../requirements/setup-project-config-file/firebase-account-setup.md" %}

{% page-ref page="../requirements/setup-project-config-file/paddle-account.md" %}

## Become our collaborator on Github

By  becoming our collaborator, you will always have access to the latest code. [Send us](https://help.mobidonia.com/#reactappbuilder) your GitHub username and purchase code. 

Then we will add you as collaborator on our repository.

[Fork it. ](https://help.github.com/en/github/getting-started-with-github/fork-a-repo)

Then you will have your own clone of the App Builder site. You can easily sync the changes from our source code.

{% hint style="info" %}
If you don't want to wait for us to give you access, you can [create new private repository with the code](https://www.softwarelab.it/2018/10/12/adding-an-existing-project-to-github-using-the-command-line/) you downloaded from Code Canyon \(Builder Folder\). But this way you lose the opportunity to sync with our source code when we release new version. 
{% endhint %}

## Publish on Netlify

[Create account on Netlify.](https://www.netlify.com/)

Click on the button "New GIT Site" 

Then select Github and connect with your account where you have forked the repository. 

For **Build command** enter: `build:netlify`

**Environment variables**

{% hint style="success" %}
* [ ] REACT\_APP\_appName              - Your Project name
* [ ] REACT\_APP\_isSaaS                    - true
* [ ] REACT\_APP\_adminEmail           - Your desired admin email
* [ ] REACT\_APP\_purchaseCode      - Your CodeCanyon purchase code
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

Now on Netlify, click on "**Deploy new site**". 

After that, you can point your domain there. 

In you project, register with the admin email you have provided. 

Set up pricing by clicking on your Avatar -&gt; Pricing. 

Then in your Paddle, go in **Developers Tools - &gt; Alerts/Week hooks**  
Paste the Url to receive web hooks   
  
****`https://YOUR_DOMAIN/.netlify/functions/paddle`  
  
****You can also enter your email, to be notified.  
****Select all Subscription events to be notified for.

{% hint style="info" %}
Your Builder Site is Active now. You can accept new customers now.
{% endhint %}

Now, let's see how you will make your client's apps. 

Learn more about our Cloud React App Builder \( We will make your client's apps \)

{% page-ref page="../cloud/cloud-vs-self-hosted.md" %}

Or make your own app producer 

**Local \(** On your computer **\)**: Makes iPhone apps \( Mac Only \) and Android Apps \(MAC or Windows\) \)   
**Automated \(** On server - fees apply **\)**: Makes Android Apps \( Linux  \)

{% page-ref page="../requirements/run-app-producer-locally.md" %}

{% page-ref page="../requirements/run-app-producer-on-server.md" %}



### Update to latest repository code.

Just go in your forked repository, and click on the "Compare button".    
Then click on the link "switching the base".

![](../.gitbook/assets/switch.png)

Then f there are changes, you will see them. Then click on the  green button "Create Pull Request". Enter Title/Description if needed and once again click on "Create Pull Request".  
Then click on the other green button "Merge pull Request".



