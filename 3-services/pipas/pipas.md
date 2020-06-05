---
title: Analytics Warehouse - Pipas
layout: template
filename: pipas.md
permalink: /services/pipas/
--- 
# Pipas - Get started

**PipaS** (**Pip**eline-**a**s-a-**S**ervice) is a tool, that helps Product teams to historicize their data that in a standardized way - company wide. With Pipas you don't have to be afraid of bringing data into BigQuery, because Pipas is

{:refdef: id="custom-ol-center"} 
- completely serverless
- autoscaling
- GCP native
- fully automated
- reliable
- real-time
{: refdef}

The biggest advantage is, that Pipas is very easy to use. All you have to do is making simple REST API calls, no matter which programming language you want to use. All the other complicated stuff - like writing a Dataflow Pipeline - is taken over by us. 

{:refdef: style="text-align: center;"}
![Fast development easier management]({{site.baseurl}}/3-services/pipas/faster-development-easier-management.png)
{: refdef}

First of all, while using **Pipas** you have to make sure that you know the difference between **stream** and **batch** pipelines. More details how to differentiate this can be found [**here**]({{site.baseurl}}/arch-principles-tenet/batch-vs-stream/).

You need to decide later in this guide if you want to use stream or batch our data. **In general we highly recommend to tune your system to be able to do stream.**
<br/>
Anyway, if batch or stream, you have some prerequisites you need to do first:

1. <a class="anchor-style" id="bo-info">**Know your Business / Data Object**</a><br/>
You must be 100% clear about the data structure of your object you are sending to us. If you aren't sure what this means, we would be happy to have a personalised chat with you. Please request a slot [**via this form.**](https://forms.gle/6MMaC1DU68grrGve7){:target="_blank"}

2. <a class="anchor-style" id="get-gcp-project">**GCP Project**</a><br/>
Your data object will be historicised within a project of the analytics context. This means, in case you already have a existing GCP project, you will get another one that is only for historicising your data. Request such a historicisation project [**via this form**](https://forms.gle/RgeJxk2qNexRcnY89){:target="_blank"}.


3. <a class="anchor-style" id="create-bq-schema">**Create BQ Schema**</a><br/>
Within the project you just received, you need to go to BigQuery and create a dataset and a schema table. This table represents the schema of your Business Object, that you are going to send to the Pipas API endpoint (Data Receiver Service). How you are going to do this, can be found in [**creating a BQ schema**]({{site.baseurl}}/services/pipas/stream/create-bq-schema/){:target="_blank"}. 

4. <a class="anchor-style" id="test-bq-schema">**Test your BQ Schema**</a><br/>
To make sure the schema table within BigQuery is a valid representation of the object you are sending to the Pipas API Endpoint (Data Receiver Service), we providing to you an Endpoint where you can test if the data object that you are sending matches with the schema table you just created. How to do this,  can be found in [**test your BQ schema**]({{site.baseurl}}/services/pipas/stream/test-bq-schema/){:target="_blank"}.

5. <a class="anchor-style" id="get-pipas">**Get your own Pipas**</a><br/>
Now you are ready to go. Just fill in [**here**](https://forms.gle/aqMAffUZVa3yj2aT8){:target="_blank"} some information, then we will double check everything. If every component is as it is expected, then you will receive an email with detailed information of what we've created for you

6. <a class="anchor-style" id="batch-vs-stream">**Batch vs Stream**</a><br/>
Based on the description above, now you need to choose what you are able to use - batch or stream. **Again, we highly recommend to tune your system that you are able to use stream.** If you need consultancy in this topic, feel free to ping [**Fabian**](mailto:seitzf@mediamarktsaturn.com).<br/>
Based on the type of data ingest you have chosen, have a look at the corresponding docs:
{:refdef: id="custom-ol-center"} 
- [**Pipas - Stream**]({{site.baseurl}}/services/pipas/stream/)
- [**Pipas - Batch**]({{site.baseurl}}/services/pipas/batch/)
{: refdef}