# Firebase Account setup

### All the data is stored in Firebase  Realtime Database and Firestore database.

In Firebase we store the information about the app, like colors, navigation etc..

And in Firestore is where our actual data is. Like menu content, categories, orders etc..

Let's get started. Create an account in Firebase with your google account.

#### Follow all the guides in the tabs. 

{% tabs %}
{% tab title="Create Project" %}
[Open Firebase](https://firebase.google.com) and Click on "Add Project". 

Accept terms, and create the project.  


![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/OrQMiE1lc2WWzKqkwPmAIJ8a5UZ1lEWSICncvyRu.png)
{% endtab %}

{% tab title="Create Realtime DB" %}
Go to Database and then click on the button called "Create database"

![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/qOYldsEBjKuXLQf1rA6YXaO8C7g58FCTEtYdUQsY.png)

After clicking on the button it should appear a window that will ask you about security rules. Click on the Start in **test mode** and after that click **Enable.**

![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/fUzpKg2ktMjb4PVCgzbRZdIubCABg0fWlSxnGHx5.png)

But for production, this is a good starting point. This will allow edit and write to all registered users.  


![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/nraH8CpL584KSYeoQZC2ADFFcd4CWYuFgY3c76Uh.png)

```text
{    "rules": {      ".read": true,       ".write": "auth !== null"    }  } 
```
{% endtab %}

{% tab title="Create Firestore" %}
Go in Databases -&gt;Cloud Firestore  


![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/rr77a8wOoaOlYzx1SstmLOda5uyNOXPPYnu0XhCN.png)

or

![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/v11spaCgNMZZwm8d1OIfixgViEI1YymXXC1Klg8G.png)

  
Then, a pop up will appear.

![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/NFDhlKFILxh38cLLOHVqaBYYp4hVjLqgdL9qid1e.png)

  
For now, use Start in test mode.
{% endtab %}

{% tab title="Create Firestorage" %}
Firebase Storage by default is not initialized. You will need to click on "Storage" and active the Firestorage Bucket.  


![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/IRTvpxbrbeo0rTTiUAmbotOTBZYZzll7JBB36p56.png)

![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/iLB5zSWpBwNfRV1nJQpPadBm4zqaeairq9E8N5OI.png)
{% endtab %}

{% tab title="Authentication" %}
After this, you should create a user in firebase for been able to login to your the app builder.

Go into firebase console and click on Authentication and after that click on **Set up sign-in method**

![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/qe83S1BmTWZnMf8Sgefmm0pKFzw93KrQs3CZ63GN.png)

Click on **Email/Password** and enable them and click Save.  
  


![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/noPpZWk9PiDRbnNRPoIu7AZezp80HVFuFWfSVSdk.png)

Now click on **Users** and now you should be able to click on **Add user**.  


![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/pHDOkSG5CpX3u7O1JogghnLEzUsmEwzSUtq53PQG.png)

Enter your email and password click Add user.
{% endtab %}

{% tab title="Google Login" %}
If you want to allow Google authentication, you have to do is to enable the Google Auth Provider as on the image below.  


![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/kQLqQN8m5ZI4jjIQkxC4Vx4si0l185VHN6cGpCIe.png)

Next, scroll below and there you should add your authorized domain. Place where the Google Login will be performed.  


![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/tfiHPrmLAtN3VwNvfJxuG9AjbVVcp342jn8ld1KY.png)
{% endtab %}
{% endtabs %}





