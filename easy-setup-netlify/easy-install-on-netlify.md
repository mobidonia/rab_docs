---
description: Netlify offer continues deployment for our Web Platfrom - For free.
---

# Install the  WEB PLATFORM

## Video Guide&#x20;

{% embed url="https://www.loom.com/share/6dce0553821444f5aef44304636d07b4" %}

> The video uses github - now we use gitlab. But steps are similar. Follow the written docs.

## Make Firebase and Paddle Account

{% content-ref url="firebase-account-setup.md" %}
[firebase-account-setup.md](firebase-account-setup.md)
{% endcontent-ref %}

{% content-ref url="paddle-account.md" %}
[paddle-account.md](paddle-account.md)
{% endcontent-ref %}

## Become our collaborator on [GitLab](https://gitlab.com)

By becoming our collaborator, you will always have access to the latest code. [Send us](https://help.mobidonia.com/#reactappbuilder) your [GitLab](https://gitlab.com) username and purchase code.&#x20;

Then we will add you as collaborator on our repository.

[Fork it. ](https://docs.gitlab.com/ee/user/project/repository/forking\_workflow.html#creating-a-fork)

Then you will have your own clone of the App Builder site.&#x20;

{% hint style="info" %}
If you don't want to wait for us to give you access, you can [create new private repository with the code you downloaded](https://docs.gitlab.com/ee/gitlab-basics/create-project.html) from Code Canyon (Builder Folder). But this way you lose the opportunity to sync with our source code when we release new version.&#x20;
{% endhint %}

## Publish on Netlify

[Create account on Netlify.](https://www.netlify.com)

Click on the button "New GIT Site"&#x20;

Then select GitLab and connect with your account where you have forked the repository.&#x20;

For **Build command** enter:   `unset CI && node fillenv.js && npm run build:cloud`

**Environment variables**

{% hint style="success" %}
* [ ] NODE\_VERSION                         - 12.22.7
* [ ] REACT\_APP\_appName              - Your Project name
* [ ] REACT\_APP\_isSaaS                    - true
* [ ] REACT\_APP\_adminEmail           - Your desired admin email
* [ ] REACT\_APP\_purchaseCode      - Your CodeCanyon purchase code
* [ ] REACT\_APP\_databasePrefix     - New Firebase DB have **-default-rtdb** prefix
{% endhint %}

{% hint style="info" %}
&#x20;Firebase have made changes in their firebase database link structure. So new databases are operating under https://PROJECTID**-default-rtdb**.firebaseio.com/. In that case, you need to deine new variable&#x20;

* [ ] REACT\_APP\_databasePrefix
{% endhint %}

{% hint style="success" %}
* [ ] REACT\_APP\_apiKey                    - Firebase Api Key ( from console.firebase.com )
* [ ] REACT\_APP\_appId                      - Firebase App ID ( from console.firebase.com
* [ ] REACT\_APP\_projectId                - Firebase Project ID ( from console.firebase.com )
{% endhint %}

{% hint style="success" %}
* [ ] REACT\_APP\_privateKey             - Private key ( from service account json )
* [ ] REACT\_APP\_serviceAccount . - client\_email ( from service account json )
{% endhint %}



{% hint style="success" %}
Now on Netlify, click on "**Deploy new site**".&#x20;
{% endhint %}

In you project, register with the admin email you have provided.&#x20;

###

### Configure React App Builder

{% tabs %}
{% tab title="Point domain to Netlify" %}
Now you site is up and running. But it is running on a subdomain from Netlify.&#x20;

And you would want to have it under your domain. ex. builder.MYDOMAIN.com

NOTE: If you use Cloud Version - we will email you instructions.&#x20;

This is supper easy. &#x20;

1. **Go in Domain Settings**

![](../.gitbook/assets/doman\_settings.png)

2\. **Add custom domain**

![](<../.gitbook/assets/add\_custom (1).png>)

![](../.gitbook/assets/entering.png)

3\. **Receive DNS info. Enter the required DNS changes in your cPanel, Domain Register or DNS provider.**

![](../.gitbook/assets/dns\_info.png)
{% endtab %}

{% tab title="Paddle Webhook" %}
In your Paddle, go in** Developers Tools - > Alerts/Week hooks**\
****Paste the Url to receive web hooks \
\
****`https://YOUR_DOMAIN/.netlify/functions/paddle`\
****

You can also enter your email, to be notified.\
****Select all Subscription events to be notified for.
{% endtab %}

{% tab title="Pricing options" %}
Set up pricing by clicking on your **Avatar -> Pricing. **

![](../.gitbook/assets/pricing.png)
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Your Builder Site is Active now. You can accept new customers now.
{% endhint %}



**Local ( **On your computer **)**: Makes iPhone apps ( Mac Only ) and Android Apps (MAC or Windows) ) \


{% content-ref url="../local/run-app-producer-locally.md" %}
[run-app-producer-locally.md](../local/run-app-producer-locally.md)
{% endcontent-ref %}



### Update to latest repository code.

With GitLab we can configure automatic code syn so your fork always has the latest code automatically. To do that.

[Send us ](https://help.mobidonia.com/#reactappbuilder)

1. GitLab Username
2. Forked project link
3. [Access token](https://gitlab.com/help/user/profile/personal\_access\_tokens.md#creating-a-personal-access-token) with **api** access

And your code and instance on Netlify will be always up to date. No manual action needed.&#x20;

