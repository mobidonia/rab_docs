# Run the app builder locally

## Configure 

Open the file Builder/firebase\_config.js. 

Here you should enter the firebase connection string.

Open config/app.js 

There enter your admin email, purchase code etc..

## Install the npm modules

Using Terminal or Command Prompt navigate to the downloaded and extracted zip. Then navigate to the folder "Builder" 

```
cd Builder
npm install
npm run start
```

This will start your project on localhost. You will get the correct link. Probably 

{% embed url="http://localhost:3000" %}



### Publish on your own hosting

After you have run the builder locally, and if it works ok you can easily publish it on your own hosting if you want. 

run

```text
npm run build
```

This command will make a **dist** folder. 

Upload this **dist** folder to your hosting. 

