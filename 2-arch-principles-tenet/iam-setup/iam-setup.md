---
title: IAM Setup
layout: template
filename: iam-setup.md
permalink: /arch-principles-tenet/iam-setup/
--- 

# IAM Setup

## Core Principles

If data is used outside a specified product team the data needs to be shared with other users. Within a team all users 
should have permissions on project level to work with the data. 

Data can be shared with other colleagues on **Dataset**, **Table** or **View** Level. 

In general all data which is shared with at least one other person needs to be exposed via the 
[Datacatalog]({{site.baseurl}}/services/data-catalog/). Data will only be shared and exposed via the datacatalog when 
defined naming conventions are met. You can find more information about it [here]({{site.baseurl}}/arch-principles-tenet/bigquery-principles/naming-conventions/)

**NOTE**: If datasets, tables or views are shared which are not exposed via the Datacataloge, all permissions will be removed 
automatically 


## How to get access to data

In general - please don't give permissions on any level in BigQuery manually if you are the data owner. As we as the analytics domain want 
to have transparency about what data is share with whom and what shareable data is available please follow this options: 

**As is:** Currently access to data can be granted by requesting the access to the data via [mail](mailto:mmst.analytics-data.access@mediamarktsaturn.com). 
There will also be a JIRA Board to request permissions, soon. 


**In the future:** We are currently working on integrating all available business and data objects in to the IAM self service 
portal. Means in the future everyone can request access to specific data via the MMS IAM portal on their own. The dataowner will then 
be notified about the access request and can then either approve or deny it.  






