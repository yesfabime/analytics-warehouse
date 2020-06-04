---
title: Analytics Warehouse - Pipas Batch
layout: template
filename: pipas-batch.md
permalink: /services/pipas/batch/
--- 
# Pipas - Batch
This is the overview of what you will get after you complete the steps below:

{:refdef: style="text-align: center;"}
![Pipas Arch - Stream]({{site.baseurl}}/2-arch-principles-tenet/pipas/batch-arch-pic.png)
{:refdef}

If your are more interested about the patterns and concepts that we have integrated into this architecture, goto [here]({{site.baseurl}}/arch-principles-tenet/ref-patterns/pipas-batch/).
<br/><br/><br/>
The current supported file types for Pipas - Batch are:
- AVRO
- PARQUET
- CSV - supported delimiters:
	- ;
	- ,
	- &#124;

There are onlw few more steps left until you will get your Pipas ready in production:

**1. Create BQ Schema**<br/>
Within the project you just received, you need to go to BigQuery and create a dataset and a schema table. This table represents the schema of your Business Object, that you are going to send to the Pipas API endpoint (Data Receiver Service). How you are going to do this, can be found in [creating a BQ schema]({{site.baseurl}}/services/pipas/stream/create-bq-schema/){:target="_blank"}. 

**2. Test your BQ Schema**<br/>
To make sure the schema table within BigQuery is a valid representation of the object you are sending to the Pipas API Endpoint (Data Receiver Service), we providing to you an Endpoint where you can test if the data object that you are sending matches with the schema table you just created. How to do this,  can be found in [test your BQ schema]({{site.baseurl}}/services/pipas/stream/test-bq-schema/){:target="_blank"}.

**3. Get your own Pipas**<br/>
Now you are ready to go. Just fill in [here](https://forms.gle/BuGNuZsSD9kHkaDq7){:target="_blank"} some information, then we will double check everything. If every component is as it is expected, then you will receive an email with detailed information of what we've created for you

**4. Test your authentication**<br/>
After the check of all information you have provided to us you will receive an email that the Pipas has been deployed successful. The last step on your side it so integrate the authentication. Examples of how to upload a file to the given GCS bucket url can be found here:
- Upload your file **manually** via the [cloud console UI](https://cloud.google.com/storage/docs/uploading-objects){:target="_blank"}
- Upload your file **programatically** via a [client library](https://cloud.google.com/storage/docs/reference/libraries#client-libraries-install-cpp){:target="_blank"}
- Upload your file **programatically** via a [Rest API calls](https://cloud.google.com/storage/docs/apis){:target="_blank"}