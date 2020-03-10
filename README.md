# Azure Data Platform - Real Time Analytics

This tutorial will give you a hands on introduction to Microsoft Azure in the perspective of a Modern Data Analytics Platform by walking you through a use case for Real Time Analytics. The tutorial is adopted from a 2 day workshop provided by Microsoft on their [Modern Data Analytics Platform](https://github.com/fabragaMS/ADPE2E).

**IMPORTANT**:

* The reference architecture proposed in this workshop aims to explain just enough of the role of each of the Azure Data Services included in the overall modern data platform architecture. This workshop does not replace the need of in-depth training on each Azure service covered.

* The services covered in this course are only a subset of a much larger family of Azure services. Similar outcomes can be achieved by leveraging other services and/or features not covered by this workshop. Specific business requirements may also ask for the use of different services or features not included in this workshop.

* Some concepts presented in this course can be quite complex and you may need to seek for more information from different sources to compliment your understanding of the Azure services covered.

![](./Media/ModernDataPlatformReferenceArchitecture.jpg)

## Document Structure
This document contains detailed step-by-step instructions on how to implement Real Time Analytics in a Modern Data Platform architecture using Azure Data Services. It’s recommended you carefully read the detailed description contained in this document for a successful experience with all Azure services. 

You will see the label **IMPORTANT** whenever a there is a critical step to the lab. Please pay close attention to the instructions given.

## Lab Prerequisites and Deployment
The following prerequisites must be completed before you start these labs:

* You must be connected to the internet;

* Use either Edge or Chrome when executing the labs. Internet Explorer may have issues when rendering the UI for specific Azure services.

* You must have a Pay-As-You-Go Azure account with administrator- or contributor-level access to your subscription. If you don’t have an account, you can sign up for an account following the instructions here: https://azure.microsoft.com/en-au/pricing/purchase-options/pay-as-you-go/. 

    <br>**IMPORTANT**: Azure free subscriptions have quota restrictions that prevent the workshop resources from being deployed successfully. Please use a Pay-As-You-Go subscription instead.

    <br>**IMPORTANT**: When you deploy the lab resources in your own subscription you are responsible for the charges related to the use of the services provisioned. For more information about the list of services and tips on how to save money when executing these labs, please visit the Cost Management section of the [Lab 0: Deploy Azure Data Platform End2End to your subscription](./Deploy/Deploy.md) page.

* This tutorial requires you to have a Power BI Pro account. If you don’t have an account you can sign up for a 60-day trial for free here: https://powerbi.microsoft.com/en-us/power-bi-pro/
  
## Lab Guide

The implementation from this tutorial forms a part of the larger modern data analytics platform architecture referenced below:

![](./Media/LabArchitecture.jpg)

### [Deploy Azure Data Platform End2End to your subscription](./Deploy/Deploy.md)

**IMPORTANT**: You should skip this Lab if you are executing the labs through subscriptions provided by CloudLabs. All Azure services will be deployed as you activate your registration.

In this section you will automatically provision all Azure resources required to complete labs 1 though to 5. We will use a pre-defined ARM template with the definition of all Azure services used to ingest, store, process and visualise data. 

The estimated time to complete this lab is: **30 minutes**.

**IMPORTANT**|
-------------|
**In order to avoid potential delays caused by issues found during the ARM template deployment it is recommended you execute Lab 0 prior to Day 1.**|

### [Ingest and Analyse real-time data with Event Hubs and Stream Analytics](./Lab/Week5/Week5.md)
In this lab you will use an Azure Logic App to simmulate a NYSE stream of stock purchase transactions. The logic app will then send the messages to Event Hubs. You will then use Stream Analytics to receive and process the stream and perform aggregations to calculate the number of transactions and amound traded in the last 10 seconds. Stream Analytics will send the results to a real-time dataset in Power BI.

The estimated time to complete this lab is: **90 minutes**.

Step     | Description
-------- | -----
![](./Media/Orange1.png) | Review the Azure Logic App logic that simmulates the NYSE transaction stream sent to EventHubs
![](./Media/Orange2.png) | Save simmulated NYSE stock transaction messages into your data lake for future analysis (cold path)
![](./Media/Orange3.png) | Send stream of NYSE stock transaction messages to Stream Analytics for real-time analytics (hot path)
![](./Media/Orange4.png) | Incorporate Stock Company reference data into your stream processing logic
![](./Media/Orange5.png) | Visualize real-time data generated by Stream Analytics with Power BI

![](./Lab/Week5/Media/Image66.png)
