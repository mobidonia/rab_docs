---
description: Netlify offer continues deployment for our App Builder - For free.
---

# Easy install on Netlify

## Video Guide 

{% embed url="https://www.loom.com/share/6dce0553821444f5aef44304636d07b4" %}

> The video uses github - now we use gitlab. But steps are similar. Follow the written docs.

## Make Firebase and Paddle Account

{% page-ref page="firebase-account-setup.md" %}

{% page-ref page="paddle-account.md" %}

## Become our collaborator on [GitLab](https://gitlab.com/)

By becoming our collaborator, you will always have access to the latest code. [Send us](https://help.mobidonia.com/#reactappbuilder) your [GitLab](https://gitlab.com/) username and purchase code. 

Then we will add you as collaborator on our repository.

[Fork it. ](https://docs.gitlab.com/ee/user/project/repository/forking_workflow.html#creating-a-fork)

Then you will have your own clone of the App Builder site. 

{% hint style="info" %}
If you don't want to wait for us to give you access, you can [create new private repository with the code you downloaded](https://docs.gitlab.com/ee/gitlab-basics/create-project.html) from Code Canyon \(Builder Folder\). But this way you lose the opportunity to sync with our source code when we release new version. 
{% endhint %}

## Publish on Netlify

[Create account on Netlify.](https://www.netlify.com/)

Click on the button "New GIT Site" 

Then select GitLab and connect with your account where you have forked the repository. 

For **Build command** enter:   `CI=false && node fillenv.js && npm run build:cloud`

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



{% hint style="success" %}
Now on Netlify, click on "**Deploy new site**". 
{% endhint %}

In you project, register with the admin email you have provided. 

### 

### Configure React App Builder

{% tabs %}
{% tab title="Point domain to Netlify" %}
Now you site is up and running. But it is running on a subdomain from Netlify. 

And you would want to have it under your domain. ex. builder.MYDOMAIN.com

NOTE: If you use Cloud Version - we will email you instructions. 

This is supper easy.  

1. **Go in Domain Settings**

![](../.gitbook/assets/doman_settings.png)

2. **Add custom domain**

![](../.gitbook/assets/add_custom%20%281%29.png)

![](../.gitbook/assets/entering.png)

3. **Receive DNS info. Enter the required DNS changes in your cPanel, Domain Register or DNS provider.**

![](../.gitbook/assets/dns_info.png)
{% endtab %}

{% tab title="Paddle Webhook" %}
In your Paddle, go in **Developers Tools - &gt; Alerts/Week hooks**  
Paste the Url to receive web hooks   
  
****`https://YOUR_DOMAIN/.netlify/functions/paddle`  
****

You can also enter your email, to be notified.  
****Select all Subscription events to be notified for.
{% endtab %}

{% tab title="Pricing options" %}
Set up pricing by clicking on your **Avatar -&gt; Pricing.** 

![](../.gitbook/assets/pricing.png)
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Your Builder Site is Active now. You can accept new customers now.
{% endhint %}

Now, let's see how you will make your client's apps. 

Learn more about our Cloud React App Builder \( We will make your client's apps \)

{% page-ref page="../cloud/cloud-vs-self-hosted.md" %}

Or make your own app producer 

**Local \(** On your computer **\)**: Makes iPhone apps \( Mac Only \) and Android Apps \(MAC or Windows\) \)   


{% page-ref page="../requirements/run-app-producer-locally.md" %}



### Update to latest repository code.

WithGitlab, we can configure automatic code syn so your fork always has the latest code automatically. To do that.

[Send us ](https://help.mobidonia.com/#reactappbuilder)

1. GitLab Username
2. Forked project link
3. [Access token](https://gitlab.com/help/user/profile/personal_access_tokens.md#creating-a-personal-access-token) with **api** access

And your code and instance on Netlify will be always up to date. No manual action needed. 



