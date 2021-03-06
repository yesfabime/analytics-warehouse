---
title: Analytics Warehouse - Services
layout: template
filename: services.md
permalink: /services/
--- 
Here you can find every service that we as a Analytics Warehouse are offering to you as a customer. Be sure you dig into the right tooling, [based on which  customer journey you are following]({{site.baseurl}}/onboarding-guide/customer-journeys).

# Data Catalog

Imagine the following situation: You want to start 
a new data-driven project. For this project you need different kinds of data. In a modern distributed multiproject GCP 
landscape you quickly lose the overview in which table in which project the desired data can be found. Wouldn't it 
be very helpful if there was a kind of *catalog* where all the data and their connection to other data are bundled?

Therefore we created our own **Data Catalog**. [Click here for further information]({{site.baseurl}}/services/data-catalog/).
<br/><br/>
**Related links to this topic:**
1. [Data Catalog Homepage](https://datacatalog.mediamarktsaturn.com/){:target="_blank"}
2. [Integrating my Business Object into Data Catalog]({{site.baseurl}}/services/data-catalog/integrating-new-bo/)


# Pipe as a Service
Our overarching goal is to build a [distributed data mesh](https://martinfowler.com/articles/data-monolith-to-mesh.html){:target="_blank"} for every datasource that lives within MediaMarktSaturn. This implies that we move from a legacy batch processing mode to a full streaming approach. A big enabler for this is a toolset that enables you to make use of streaming pipelines without getting in touch with too much details. This is the reason why we introduce Pipe as a Service. [Click here for further information]({{site.baseurl}}/services/pipas/).
<br/><br/>
**Related links to this topic:**
1. [Request a slot for designing your data object](https://forms.gle/6MMaC1DU68grrGve7){:target="_blank"}
2. [Request a GCP project for your Analytics use-case](https://forms.gle/RgeJxk2qNexRcnY89){:target="_blank"}
3. [**Pipas**]({{site.baseurl}}/services/pipas/)
	- [Create a BQ schema via the BigQuery UI]({{site.baseurl}}/services/pipas/stream/create-bq-schema/#create-bq-schema)
	- [Test your BQ schema via the customer check]({{site.baseurl}}/services/pipas/stream/test-bq-schema/#test-bq-schema)
	- [Get your own Pipas - Stream](https://forms.gle/aqMAffUZVa3yj2aT8){:target="_blank"}
	- [**Pipas - Stream**]({{site.baseurl}}/services/pipas/stream/#pipas-stream)
		- [Test your authentication for your stream pipas]({{site.baseurl}}/services/pipas/stream/test-auth/#test-auth){:target="_blank"}
	- [**Pipas - Batch**]({{site.baseurl}}/services/pipas/batch/#pipas-batch)
		- [Test your authentication for your batch pipas]({{site.baseurl}}/services/pipas/batch/test-auth/#test-auth){:target="_blank"}


# Stackdriver to MS Teams connector
We use Stackdriver as our logging, monitoring & alerting tool. Therefore we highly rely on getting all events fired to the chat tools we are using. As MMS determined that MS Teams is the future of chat & video collaboration, we needed a connector that fires the messages directly in MS Teams channels. [Click here for further information]({{site.baseurl}}/services/stackdriver-msteams/).


# Reporting Gallery
The scope of our Analytics Warehouse is not limited on high sophisticated Analytics Use-Cases but also imply reporting cases. For this, we are providing you an overview of all Dashboards that are available through the Analytics Warehouse. [Click here for further information](https://datastudio.google.com/u/0/reporting/16WoSqAvzt1imDrpPF8BCdNrpU4pS5lIF/page/QnMPB){:target="_blank"}.