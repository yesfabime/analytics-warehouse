---
title: Analytics Warehouse - Pipas Stream
layout: template
filename: create-bq-schema.md
permalink: /services/pipas/stream/create-bq-schema/
--- 
# Creating a BQ Schema

Go to [https://console.cloud.google.com/bigquery](https://console.cloud.google.com/bigquery){:target="_blank"} in your project. 

Click on your project on the left side and afterwards on **CREATE DATASET**:
{:refdef: style="text-align: center;"}
![Create Dataset - 1]({{site.baseurl}}/3-services/pipas/create-bq-schema/screen-1.png)
{: refdef}
{:refdef: style="text-align: center;"}
![Create Dataset - 2]({{site.baseurl}}/3-services/pipas/create-bq-schema/screen-2.png)
{: refdef}

Once you've created the dataset you can create the table. Click on the left side on the created dataset with the name "schema_for_beverages_sales" and then on **CREATE TABLE:** 
{:refdef: style="text-align: center;"}
![Create Table - 1]({{site.baseurl}}/3-services/pipas/create-bq-schema/screen-3.png)
{: refdef}

Afterwards you have to specify the schema of your data as an BigQuery table. Please make sure that the schema is correct and contains all of columns which are possible. Otherwise Pipas is not able to stream data into BigQuery. Please be aware of **partitioning and clustering** of your table. If you have a timestamp column, please specify the table partitioning on this column. This is needed because of cost and performance reasons.  If you also have a country and/or a brand column within the data, please select these columns for clustering - please note that clustering is only available in addition to partitioning 

{:refdef: style="text-align: center;"} 
![Create Table - 4]({{site.baseurl}}/3-services/pipas/create-bq-schema/screen-4.png) 
{: refdef} 

Click on **Create Table** and you're finished.

The schema table is only needed to provide the schema for Pipas and for testing out the pipeline with your data. Pipas will copy schema, clustering and partitioning of this table and creates a new one for the historization afterwards.

If you have arrays in your data structure, then you need to consider using nested fields. How they can be used [can be found here](https://cloud.google.com/bigquery/docs/nested-repeated).