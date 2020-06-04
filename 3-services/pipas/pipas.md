---
title: Analytics Warehouse - Pipas
layout: template
filename: pipas.md
permalink: /services/pipas/
--- 
# Pipas - Get started

**PipaS** (**Pip**eline-**a**s-a-**S**ervice) is a tool, that helps Product teams to historicize their data that in a standardized way - company wide. With Pipas you don't have to be afraid of bringing data into BigQuery, because Pipas is:

{:refdef: id="custom-ol-center"} 
- completely serverless
- autoscaling
- GCP native
- fully automated
- reliable
- real-time (stream)
{: refdef}

The biggest advantage is, that Pipas is very easy to use. All you have to do is making simple REST API calls, no matter which programming language you want to use. All the other complicated stuff - like writing a Dataflow Pipeline - is taken over by us. 

{:refdef: style="text-align: center;"}
![Fast development easier management]({{site.baseurl}}/3-services/pipas/faster-development-easier-management.png)
{: refdef}

First of all, while using **Pipas** you have to make sure that you know the difference between **stream** and **batch** pipelines:

- Batch (bounded data):<br/>
    *Batch processing is where the processing happens of blocks of data that have already been stored over a period of time. For example, processing all the transaction that have been performed by a major financial firm in a week. This data contains millions of records for a day that can be stored as a file or record etc. This particular file will undergo processing at the end of the day for various analysis that firm wants to do.* 

    → In Batch you process one (or sometimes more than one) file with a lot of rows (>1).

- Stream (unbounded data):<br/>
    *Stream processing is a golden key if you want analytics results in real time. Stream processing allows us to process data in real time as they arrive and quickly detect conditions within small time period from the point of receiving the data. Stream processing allows you to feed data into analytics tools as soon as they get generated and get instant analytics results.* 

    → In Stream you process one message - in general one json-file per request. 
<br/>
[Source: [Big Data Battle : Batch Processing vs Stream Processing](https://medium.com/@gowthamy/big-data-battle-batch-processing-vs-stream-processing-5d94600d8103){:target="_blank"}]


Based on the description above, you need to decide later in this doc if you want to use stream or batch our data. **In general we highly recommend to tune your system to be able to do stream.**
<br/>
Anyway, if batch or stream, you have some prerequisites you need to do first:

1. **Know your Business / Data Object**<br/>
You must be 100% clear about the data structure of your object you are sending to us. If you aren't sure what this means, we would be happy to have a personalised chat with you. Please request a slot [via this form.](https://forms.gle/6MMaC1DU68grrGve7){:target="_blank"}

2. **GCP Project**<br/>
Your data object will be historicised within a project of the analytics context. This means, in case you already have a existing GCP project, you will get another one that is only for historicising your data. Request such a historicisation project [via this form](https://forms.gle/RgeJxk2qNexRcnY89){:target="_blank"}.

3. **Batch vs Stream**<br/>
Based on the description above, now you need to choose what you are able to use - batch or stream. **Again, we highly recommend to tune your system that you are able to use stream.** If you need consultancy in this topic, feel free to ping seitzf@mediamarktsaturn.com. 
Based on the type of data ingest you have chosen, have a look at the corresponding docs:
{:refdef: id="custom-ol-center"} 
- [Pipas - Stream]({{site.baseurl}}/services/pipas/stream/)
- [Pipas - Batch]({{site.baseurl}}/services/pipas/batch/)
{: refdef}