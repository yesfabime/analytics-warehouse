---
title: GCP Project Setup
layout: template
filename: gcp-project-setup.md
permalink: /arch-principles-tenet/gcp-project-setup/gcp-project-setup
--- 


# GCP Project Setup 

This section gives an overview how the GCP project structure within GCP looks like and why it looks like it is. 

## Multi vs Single Project Setup 


In this point we're following the recommendations from Google how to structure the project setup within GCP. 
Therefore we're having a Multi Project Setup. 

Here are some reasons why this is important to stick to: 

![Project organization best practice]({{site.baseurl}}/2-arch-principles-tenet/gcp-project-setup/project-organization.png "Project Organization by Google")


- Billing isolation: Possibilities for different billing accounts, easy cost visibility per workload and environment

- Quotas and limits: Separate by environment and workloads

- Administrative complexity: Access management separate by environment and workload, with additional management overhead

- Blast radius: Misconfiguration issues only impact workloads specific environments

- Separation of duties: Business units and data sensitivity classification are separate 

- Cross project network traffic- VPN/ VPC is shared in a multi project setup

- Easier to enforce least privilege access on per project level while still having low complexity in maintaining IAM roles 


## Environment Stages

There is a best practice we're following when it comes to development stages. We see three stages as sufficient within the analytics 
domain. 

![Project stages best practice]({{site.baseurl}}/2-arch-principles-tenet/gcp-project-setup/stages.png "Project Stage Analytics Domain")



As there is any need of additional stages just feel free to contact the folder administrator. 


## MMS specific setup of the GCP organization 

The MMS GCP structure is starting with an organization node where all other folders or projects are depending on. 
There are some restrictions made on organization leven by Cloud Strategy & Governance and our Security Department which are 
inherited by every other folder. There are several folder depending on the different business units e.g.: 

- Analytics
- SAP 
- Digital Platform 
- Webshop Foundation 
- Cloud Foundation 

There are folder admins for every of these folders who take care of the rules coming by above mentioned instances which can not be 
inherited because of technical constrains and they also organize the project structure within the folder. For analytics this is Fabian Seitz
and Tobias Hoke. 

![Project stages best practice]({{site.baseurl}}/2-arch-principles-tenet/gcp-project-setup/stages.png "Project Stage Analytics Domain")

