# Can't login, stays on login screen

**Problem**

After you have entered your email/pass, you are not redirected to the admin backend.In the [console](https://mobidonia.support-hub.io/articles/how-to-open-the-developer-console), you receive this if you try to register a new user.

![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/ktMq6nIZCKrbDStTQ1ThkOl1U1MPh3R7TB68wy1T.png)

**Cause**

Your Firebase Database permissions are not correctly set up.

**Solution**

Change your Real-time Database rules

Suggested permissions are described in step **Create a real-time database**

![](https://support-hub--assets.s3.eu-west-2.amazonaws.com/assets/74/images/OEYxI2Bc5CMvFCqouiETskOcMbexWxkyMfBkLFiA.png)

