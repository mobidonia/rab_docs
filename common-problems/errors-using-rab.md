---
description: Common problems using rbainstaller
---

# Errors using rab

## Send us info for your computer on your ticket

run in terminal

`rab`

And then Select **Management** -&gt; **Show My Info**

## Error on deploying cloud functions.

Run the following series of actions in your terminal / cmd

```text
npm i -g firebase-tools
npm i -g rabinstaller
cd Cloud Functions
npm install
cd functions
npm install
cd ..
cd ..
rab 
```

And select "Deploy cloud functions"

## Error on deploying landing page

Run the following series of actions in your terminal / cmd

```text
npm i -g firebase-tools
npm i -g rabinstaller
npm install
rab 
```

And select your desired action

