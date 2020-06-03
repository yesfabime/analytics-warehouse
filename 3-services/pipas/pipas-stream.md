---
title: Analytics Warehouse - Pipas Stream
layout: template
filename: pipas-stream.md
permalink: /services/pipas/stream/
--- 
# Pipas - Stream
Great, stream is the right choice! This is the overview of what you will get after you complete the steps below:

{:refdef: style="text-align: center;"}
![Pipas Arch - Stream]({{site.baseurl}}/2-arch-principles-tenet/pipas/stream-arch-pic.png)
{:refdef}

If your are more interested about the patterns and concepts that we have integrated into this architecture, goto [here]({{site.baseurl}}/arch-principles-tenet/ref-patterns/pipas-stream/).
<br/><br/><br/>
The following few steps are left until you will get your Pipas ready in production.

**1. Create BQ Schema**<br/>
Within the project you just received, you need to go to BigQuery and create a dataset and a schema table. This table represents the schema of your Business Object, that you are going to send to the Pipas API endpoint (Data Receiver Service). How you are going to do this, can be found in [creating a BQ schema]({{site.baseurl}}/services/pipas/stream/create-bq-schema/){:target="_blank"}. 

**2. Test your BQ Schema**<br/>
To make sure the schema table within BigQuery is a valid representation of the object you are sending to the Pipas API Endpoint (Data Receiver Service), we providing to you an Endpoint where you can test if the data object that you are sending matches with the schema table you just created. How to do this,  can be found in [test your BQ schema]({{site.baseurl}}/services/pipas/stream/test-bq-schema/){:target="_blank"}.

**3. Get your own Pipas**<br/>
Now you are ready to go. Just fill in [here](https://forms.gle/aqMAffUZVa3yj2aT8){:target="_blank"} some information, then we will double check everything. If every component is as it is expected, then you will receive an email with detailed information of what we've created for you

**4. Test your authentication**<br/>
After the double checkup from our side is done, we will provide you a GCP service account that you can use for authentication. Code snippets of how to intergate authentication and how to test your auth, can be found [here]({{site.baseurl}}/services/pipas/stream/test-auth/){:target="_blank"}.

**5. You are completely ready to use your pipe**<br/>
Congratulations - now you have the ability to stream your data in realtime to the Analytics Warehouse. This is an huge step for you and for us. Thanks for being now on the Analytics train!