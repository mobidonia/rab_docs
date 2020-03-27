# Stuck on App Prioducer

**Problem**: When I run app producer, it get's stuck on this

```text
? What you want to do next? Make Android app
? What is the APP ID you want to make? 1

/rab_pointers/data/1
\ Fetching App Data..
/saasapps/xxxxxxxxxxxxxxx/zzzzzzzzzzzzz
```

**Reason 1**:  Google has changed firebase permissions on their own.  
**Reason 2**: Bug in version 13.1

\*\*\*\*

**Solution 1**: 

1.Go in your [Firebase Console](https://console.firebase.google.com/)  
2. Locate your project  
3. Go in Firebase Realtime Database Rules and Firestore Datbase Rules  
4. They should be like on our guide bellow.

**Solution 2:**

Download the latest code from CodeCanyon. There we have the fix in the file Mobile App/Producer/produce.js

{% page-ref page="../easy-setup-netlify/firebase-account-setup.md" %}



