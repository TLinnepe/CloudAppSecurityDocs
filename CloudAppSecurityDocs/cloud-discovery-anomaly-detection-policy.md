---
# required metadata

title: Create a Cloud Discovery anomaly detection policy in Cloud App Security | Microsoft Docs
description: This topic provides information about how to work with Cloud Discovery anomaly detection policies.
keywords:
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 4/22/2018
ms.topic: conceptual
ms.prod:
ms.service: cloud-app-security
ms.technology:
ms.assetid: eaf73af0-7610-4903-b656-8d90b1d2b18c

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: reutam
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

*Applies to: Microsoft Cloud App Security*


# Cloud Discovery anomaly detection policy
This article provides reference details about policies, providing explanations for each policy type and the fields that can be configured for each policy.  
  
## Cloud discovery anomaly detection policy reference  
A Cloud discovery anomaly detection policy enables you to set up and configure continuous monitoring of unusual increases in cloud application usage. For each cloud application, increases in downloaded data, uploaded data, number of transactions and number of users are considered. Each increase is compared to the normal usage pattern of the application as learned from past usage. The most extreme increases trigger security alerts.  
  
For each policy you can set filters that enable you to selectively monitor application usage, based on an application filter, selected data views, and a selected start date. You can also set the sensitivity, which enables you to set how many alerts the policy should trigger.  

For each policy, set the following parameters:

1. Decide if you want to base the policy on a template, relevant policy templates are the **Anomalous behavior in discovered users** template that alerts when anomalous behavior is detected in discovered users and apps, such as: large amounts of uploaded data compared to other users, large user transactions compared to the user's history. You can also select the **Anomalous behavior of discovered IP addresses** template, which alerts when anomalous behavior is detected in discovered IP addresses and apps, such as: large amounts of uploaded data compared to other IP addresses, large app transactions compared to the IP address's history. 
 
2. Provide a **Policy name** and **Description**.  

3. Create a filter for the apps you want to monitor by clicking <strong>Add filter</strong>. 
   You can select a specific app, an app <strong>Category</strong>, or filter by <strong>Name</strong>, <strong>Domain, and **Risk factor</strong>, and click <strong>Save</strong>.

4. Under **Apply to**, set how you want the usage to be filtered. The usage being monitored can be filtered in two different ways:  
  
    -   Continuous reports – select whether to monitor **All continuous reports** (default), or choose **Specific continuous reports** to monitor.  
  
        -   When selecting **All continuous reports**, each usage increase is compared to the normal usage pattern as learned from all the data views.  
  
        -   When selecting **Specific continuous reports**, each usage increase is compared to the normal usage pattern as learned from the same data view as the increase was observed in.  
  
    -   **Users and IP addresses** – every cloud application usage is associated either with a user, an IP address, or both.  
  
        -   Selecting **Users** ignores the association of application usage with IP addresses if there is any.  
  
        -   Selecting **IP addresses** ignores the association of application usage with users if there is any.  
  
        -   Selecting **Users and IP addresses** (default) considers both associations, but may produce duplicate alerts when there is a tight correspondence between users and IP addresses.
    -   Trigger alerts only for suspicious activities occurring after date – any increase in application usage before the selected date is ignored. However, activity from before the selected date is learned for the purpose of establishing the normal usage pattern.  
  
5. Under **Alerts**, you can set the alert sensitivity. There are a number of ways to control the number of alerts triggered by the policy:  
  
    -   The **Select anomaly detection sensitivity** slider – Trigger alerts for the top X anomalous activities per 1,000 users per week. The alerts are triggered for the activities with the highest risk.  
  
    -   **Daily alert limit** – restrict the number of alerts raised on a single day. You can select whether to **Send alert as email**, **Send alert as text message or both**. Messages sent by text message are limited to 10 per day, for the UTC time zone, meaning that the 10 message limit resets at midnight in the UTC time zone.

    - You can also select the option to **Use your organization's default settings**, which fills in the **Daily alert limit**, email, and text message settings from your organization's default settings. To set the default, fill out the **Alert configuration** settings and click **Save these alert settings as the default for your organization**.

6. Click **Create**.

7. Like with all policies, you can **Edit**, **Disable**, and **Enable** the policy by clicking the three dots at the end of the row in the **Policies** page. By default, when you create a policy it is enabled.

## See Also  
[Daily activities to protect your cloud environment](daily-activities-to-protect-your-cloud-environment.md)   

[Premier customers can also choose Cloud App Security directly from the Premier Portal.](https://premier.microsoft.com/)  
  
  