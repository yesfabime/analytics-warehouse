---
title: Analytics Warehouse - Data Catalog
layout: template
filename: overview.md
permalink: /services/data-catalog/
--- 
# Data Catalog - Overview

We started first with a look at the [Google Cloud Data Catalog](https://cloud.google.com/data-catalog). 
This is a very great GCP tool, but for our purposes it was not mature enough (as of September 2019). 
There was one big thing missing: How are data objects  related to other data objects? Is there any connection to others 
at all? 

First of all it's important to know, that our Data Catalog is based on **Business Objects (BO)** and  **Data Objects**
 [Click here for further information]({{site.baseurl}}/services/data-catalog/).

Our Data Catalog can be seen as the entry point for every analytical use-case. It simplifies and speeds up the life of 
everyone who wants to work with data, because our Data Catalog brings all metadata information about Business Objects 
from all GCP projects to one place.

With the following features, our Data Catalog is a real relief to get quick access to the data you want: 

- **Visualization** of Business Object realationships: You immediately get an overview of which Business Object have a 
relationship with another. That means, which Business Object can be joined with another one. 

- **Metadata information** of all Business Objects: For every Business Object, you can see at a glance which columns an 
object contains (with description). So you easily find the information you need for your purpose. 

- **SQL Generator**: This features speeds up your way to the real data. You just have to select the date range for which
you want to have the data, your billing GCP project and your Business Object. As a result you will get an ready to use
BigQuery query, you don't have to care about the GCP project_id, dataset_id and table_id. Just take the query and execute 
it (if you are allowed to do this)! <br/> <br/>
Additionally you can add a Business Object to your selected Business Object which 
have a relationship (doesn't matter if a direct connection or with one or more Business Objects in between) to each other. 
The SQL Generator creates a ready to use SQL with all needed Business Objects joined together. So you don't have to 
care about the columns you have to join on. <br/> <br/>
But attention, the SQLs you will get are just templates. They are ready to execute, but you may need to adjust 
it to fit your use case. I. e. in the most of the use-cases you do not need all columns, so please remove all columns
from the query you don't need, it saves you a lot of costs! (TODO Add link to BQ) <br/> <br/>
Furthermore you have to be aware of which country/countries you want to consider. By default, if you select no specific country, 
you will get all available countries (of course only if the Business Object distinguishes between countries). 


- **IAM**: Because our Data Catalog just saving metadata information (not real data) from the Business Objects, we 
don't have to care about Identity and Access Management (IAM).If you have had a query created, it can only be executed if you have the corresponding BigQuery rights.
 That means for us: All the IAM stuff is handled by the BigQuery IAM of the Business Object owners. 

 
That's great, isn't it? Have we aroused your interest? [Try it out](https://datacatalog.mediamarktsaturn.com/){:target="_blank"}!


If your are more interested about the underlying architecture, goto [**here**]({{site.baseurl}}/services/data-catalog/architecture/).




