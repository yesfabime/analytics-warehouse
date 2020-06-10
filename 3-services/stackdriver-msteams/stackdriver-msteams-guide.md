---
title: Analytics Warehouse - Stackdriver MS Teams
layout: template
filename: stackdriver-msteams.md
permalink: /services/stackdriver-msteams/
--- 
# Guide to Stackdriver - MS Teams Connector
Typically Stackdriver provides a lot of native notification channels to various tools. Unfortunately there is no native MS Teams connector available. This was the reason why we've created a serverless connector that forwards messages from Stackdriver directly to a respective MS Teams Channel. If you want to get more in touch with the implementation details, feel free to [read here more about it]({{site.baseurl}}/arch-principles-tenet/stackdriver-msteams/).<br/>
To get an overview, you can have a look at our architectural diagram:
{:refdef: style="text-align: center;"}
![Fast development easier management]({{site.baseurl}}/2-arch-principles-tenet/stackdriver-msteams/Stackdriver-MSTeams-Integration.png)
{: refdef}



So what you have to do if you want to use our service? I will show you step by step: 

1. Go to Microsoft Teams and navigate to the channel where you want to add the webhook 
2. Select (•••) More Options from the top navigation bar.
3. Choose **Connectors** from the drop-down menu and search for **Incoming Webhook**.
    {:refdef: style="text-align: center;"}
    ![search_for_incoming_webhook.png]({{site.baseurl}}/3-services/stackdriver-msteams/search_for_incoming_webhook.png)
    {: refdef}
4. Select the **Configure button**, provide a name, and, optionally, upload an image avatar for your webhook.
5. The dialog window will present a unique URL that will map to the channel. Make sure that you copy and save the URL— you will need to provide it to our service!! 
    {:refdef: style="text-align: center;"}
    ![copy_webhook_url.png]({{site.baseurl}}/3-services/stackdriver-msteams/copy_webhook_url.png)
    {: refdef}
6. Select the Done button. The webhook will be available in the team channel.
7. Go to our Web Ui [Web UI](https://stackdriver-msteams-connector-web-ui-lbxce2mtxa-ew.a.run.app){:target="_blank"} and sign in with your MediaMarktSaturn Google Account. 
8. Fill in the Textfields in our Web UI. Here you need your copied webhook URL, your GCP Project ID (where you want to deploy our connector.  **Attention**, Stackdriver must be enabled in your project.) and your custom display name. 
     {:refdef: style="text-align: center;"}
    ![filled_forms.png]({{site.baseurl}}/3-services/stackdriver-msteams/filled_forms.png)
    {: refdef}
9. Click on **Create Connector.** 
10. Wait a few seconds.
11. Your connector is now created.
    {:refdef: style="text-align: center;"}
    ![connector_created_successfully.png]({{site.baseurl}}/3-services/stackdriver-msteams/connector_created_successfully.png)
    {: refdef}
12. Go to [Stackdriver](https://console.cloud.google.com/monitoring){:target="_blank"} in your project
13. Navigate to Notification Channels. Under the Section **Cloud Pub/Sub** you can see your new notification channel. 
    {:refdef: style="text-align: center;"}
    ![stackdriver_notification_channels.png]({{site.baseurl}}/3-services/stackdriver-msteams/stackdriver_notification_channels.png)
    {: refdef}
14. Now you're done! You can choose this channel for every policy you want have alerts in your MS Teams channel. A message in Teams looks like that (I've added an Icon): 
    {:refdef: style="text-align: center;"}
    ![test_message.png]({{site.baseurl}}/3-services/stackdriver-msteams/test_message.png)
    {: refdef}






