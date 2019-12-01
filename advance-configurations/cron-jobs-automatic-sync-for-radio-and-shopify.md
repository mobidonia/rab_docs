# Cron Jobs - Automatic sync for Radio and Shopify

Some functions are required to be called on an interval. Example of the syncing function for Radio, Shopify Data. 

That is why we need to define our own schedule of calling these functions.

**Cron Job Caller**

You have the following options to create cron jobs. 

1. WebMin Cron job - https://YOUR\_DOMAIN:10000

2. Google Scheduler - https://cloud.google.com/scheduler/ \( free quota of three \(3\) jobs per month \) 

3. Your hosting Cron - If you have your own hosting, it is common that you can create cron jobs.

4. Use other 3rd part cloud cron caller ex. [https://cron-job.org/en/](https://cron-job.org/en/) or [https://azure.microsoft.com/en-us/services/scheduler/](https://azure.microsoft.com/en-us/services/scheduler/) or search for any other. 

#### **Cron Job creation**

Let's create a cron job. First, you need to go in your firebase functions and location the HTTP function that needs to be called.

![](../.gitbook/assets/screenshot%20%281%29.png)

Copy the function link. And create a cron job on an interval you wish. ex. every 1min

This can help

[https://cloud.google.com/scheduler/docs/configuring/cron-job-schedules](https://cloud.google.com/scheduler/docs/configuring/cron-job-schedules)

The cron in WEbMin should look like this

![](../.gitbook/assets/screenshot%20%282%29.png)

The cron in Google Scheduler Can look like this

![](../.gitbook/assets/screenshot%20%284%29.png)

Now my radios data will update every 1 min. 

You should do cron jobs for Shopify Sync And Radio Sync. 

For Shopify sync, the sync interval can be bigger, ex. 1hour or more.

