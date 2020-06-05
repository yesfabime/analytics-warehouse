---
title: BigQuery principles - Naming conventions
layout: template
filename: naming-conventions.md
permalink: /arch-principles-tenet/bigquery-principles/naming-conventions/
--- 

# BigQuery Principles - Naming Conventions

We defined some naming conventions for data which is shared and can be used by other departments or colleagues within 
MediaMarktSaturn. 

The general naming conventions for **Datasets**, **Tables** and **Views** is &rarr;  **Snake Case**

Data which can or should be shared needs also be exposed via the DataCatalog. 

To expose data and make it accessable the following conventions need to be concidered: 

## Datasets 

````python
BO_[business-object-name]

e.g. BO_customer_order_online
````

As we're only talking of Business Objects in the context of sharing data, the BO stands for Business Object. 

## Tables 

As should not be shared, only views there is no specific naming convention for tables at all. 
This means the only only convetions here is the **Snake Case**:

````python
this_is_my_table
````

## Views 

As views are shared and should be recognizable as views in the first sights the naming of views start with and 
underscore: 

````python
v_[business-object-name]
````

Views can be used to share only specific data from a base table, therefore the convention is to determine 
the data more exactly with a suffix. 

Here are some examples: 

````python
View on country level: 

v_[business-object-name]_DE
v_[business-object-name]_AT



Views on sales line level: 

v_[business-object-name]_MM
v_[business-object-name]_SE

````

