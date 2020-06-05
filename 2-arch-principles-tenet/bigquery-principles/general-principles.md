---
title: BigQuery principles - Naming conventions
layout: template
filename: naming-conventions.md
permalink: /arch-principles-tenet/bigquery-principles/general-principles
--- 


# General BigQuery Principles

BigQuery offers a lot of possibilities to store data efficient. Therefore here are some general principles /
beste practices of how to work with Bigquery: 


## Partitioning

Partitioning is a usefull tool to make queries more efficient and reduce query costs. It is basically a 
limitation of the data to query on specific days of data. 

In most cases only a specific timerange of data is necessary to be queried e.g. the last month of our sales. 
Instead of querying the whole sales table you add the **where** clause to the statement to limit the timerange
the data is queried. BigQuery will then only touch the data which is relevant to this timerange. 

Therefore we want everyone to partition their tables on a relevant timestamp. If the data doesn't contain such 
a timestamp just add a 'last-update-timestamp' or 'insert-timestamp' to the data row and then set the partitioning
of the table on that timestamp.

Here you can find information of how to create [partitioned tables](https://cloud.google.com/bigquery/docs/partitioned-tables)

**Important:**

As we're only sharing data on view level - please make sure to expose also the partition column to the view. 
That means that the partitioning filter can also be applied when the view on the table and not the table it self 
gets queried. 

Here is an example of how to expose the partitioning field via SQL: 

````sql
EXTRACT(DATE
  FROM
    _PARTITIONTIME) AS partition_date
````


## Clustering 

When a table is partitioned it is also possible to cluster the table. Clustering is a way to make your query even more performant
and less cost intensive then only partitioning. 

Clustering cuts the table virtual into business relevant pieces. One example is the clustering in country level. 
In a lot of use cases it can be the case that only data of a specific country is relevant for the use case. Here 
it would make sense to cluster the table bases on a country flag column. 

If there's any column which you see as a relevant clustering option we encourage you to cluster the table. 
Here are some more information of how to create [clustered tables](https://cloud.google.com/bigquery/docs/creating-partitioned-tables)

## Metadata

If data is shared and exposed via the Datacatalog we enforce you to fill in every metainformation BigQuery offers 
to describe the data in more detail: 

- Dataset description 
- Table description 
- Table info
- Column description

Even if it is only one sentence - a description makes it more easier for everyone to work with the data. All the information 
which is given in the metadata will be exposed to the datacatalog and helps to bring transparency. 


## Data exposure via views 

In general data is only share via views - not on table base (team external of course). This prevents any unwanted 
data manipulation on the base data. Therefore we will only expose views within the datacatalog. 

The charming effect of views is also that views can limit the data which can be seen from the base table. Simple 
example: 

We have a sales table of all countries, the spanish colleagues are only allowed to see sales data from ES 
with the help of view you can filter in the view select statement to only ES data and provide this view to the 
spanish colleagues. 

Here are more information about how [views can be created](https://cloud.google.com/bigquery/docs/views)

It is also common practice to create cascading views. This means you can also create a new view based on another 
view if the use case makes it necessary to limit the data once more. 

