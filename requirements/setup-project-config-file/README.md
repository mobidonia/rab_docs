# Setup project config file

Now, unzip the zip file that you got from CodeCanyon. 

Open the folder with [Visual Studio Code](https://code.visualstudio.com).

![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/3aKiHW22V7xW0i9SKqTfnfKyojFMMbuHhzo9B5oq.png)

In the file structure, locate **project\_config.json**. 

Let's go step by step and fill all the necessary things

{% tabs %}
{% tab title="App Name" %}
appName is the name of your project.
{% endtab %}

{% tab title="Purchase Code" %}
You can find the **purchaseCode** in [CodeCanyon Download Page](https://codecanyon.net/downloads?utf8=%E2%9C%93&filter_by=codecanyon.net&sort_by=Date+Purchased&order=desc&page=1).
{% endtab %}

{% tab title="Admin Email" %}
Admin email  - is your personal email, that you will use to admiinister the site.   
Later, create this user is Firebase.
{% endtab %}

{% tab title="Firebase Element" %}
Follow this link to create account in Firebase.

{% page-ref page="firebase-account-setup.md" %}

Then go in Project settings and create a web app.

![](../../.gitbook/assets/project_settings_web_app.png)

Set all the values, from the project config into the Firebase Element in project\_config.js
{% endtab %}

{% tab title="Pricing" %}
Follow this link to learn how to make a Paddle Account. 

{% page-ref page="paddle-account.md" %}

When you have your Paddle account ready, and you have set your pricing plans, copy and set the values in **project\_config.json.** 

You also need to replace the **vendor\_id**
{% endtab %}

{% tab title="SMTP" %}
SMTP is used to send email when the app producer has made the app. Follow the docs on the following link.

{% page-ref page="smtp-account.md" %}

Fill all the required fields for the SMTP settings in **project\_config.json**
{% endtab %}
{% endtabs %}

When you have finished all the steps, the JSON file should look like this.

![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/S1qSHGsJkrVbqAHyo15dSnFrBYx8gJz2rjD5mxIW.png)

Next, you can continue on Setup and deploy

{% page-ref page="../../setup-and-deploy-the-project/setup-your-project.md" %}

