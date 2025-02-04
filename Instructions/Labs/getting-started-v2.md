# Secure Windows Servers Azure Arc & Microsoft Defender

### Overall Estimated Duration: 8 hours

## Overview

In this hands-on lab, you will explore security operations and hybrid cloud management using Microsoft security and monitoring tools. You will start by using Azure Migrate: Discovery and Assessment to onboard on-premises Hyper-V VMs to Azure Arc, enabling centralized management of hybrid environments. You will then enable Microsoft Defender for Cloud to enhance cloud workload protection and respond to security alerts. Moving to Microsoft Sentinel, you will integrate log data from multiple sources, including Microsoft 365, non-Azure VMs, network appliances, and Linux VMs using CEF and Syslog connectors. Additionally, you will connect Microsoft Defender XDR to Microsoft Sentinel for a unified security operations experience. Finally, you will use Kusto Query Language (KQL) to analyze log data, visualize insights, and conduct threat hunting.

## Objective

This lab is designed to equip participants with hands-on experience in using Azure OpenAI to build powerful AI applications. By completing this lab, participants will learn to:

- **Onboard Windows Servers to Azure Arc**: Onboard on-premises servers to Azure Arc-enabled servers for centralized management and governance.
- **Enable Microsoft Defender for Cloud**: Configure security monitoring and threat protection by setting up a Subscription, creating a Log Analytics Workspace, enabling Microsoft Defender for Cloud, installing Azure Arc on an on-premises server, and implementing security measures to protect it.
- **Mitigate threats using Microsoft Defender for Cloud**: Enhance security and compliance awareness by exploring regulatory compliance, assessing security posture and recommendations, and mitigating security alerts effectively.
- **Connect data to Microsoft Sentinel using data connectors**: Access the Microsoft Sentinel workspace and integrate key security data sources by connecting Microsoft Entra ID, Entra ID Protection, Microsoft Defender for Cloud, and Azure Activity connectors.
- **Connect Windows devices to Microsoft Sentinel using data connectors**:


## Prerequisites

- Basic knowledge of on-premises Hyper-V infrastructure
- Familiarity with Security Information and Event Management (SIEM) concepts
- Basic understanding of KQL syntax for querying and analyzing logs

## Architecture


## Architecture Diagram



## Explanation of Components

The architecture for this lab involves several key components:

-
-
-
-

## Getting started with the lab
 
Welcome to your Secure Windows Servers Azure Arc & Microsoft Defender Workshop! We've prepared a seamless environment for you to explore and learn about Azure services. Let's begin by making the most of this experience:
 
## Accessing Your Lab Environment
 
Once you're ready to dive in, your virtual machine and lab guide will be right at your fingertips within your web browser.
 
   ![](media/labguide-1.png "Lab Environment")

### Virtual Machine & Lab Guide
 
Your virtual machine is your workhorse throughout the workshop. The lab guide is your roadmap to success.
 
## Exploring Your Lab Resources
 
To get a better understanding of your lab resources and credentials, navigate to the **Environment** tab.
 
   ![](media/miw(3-3).png)
 
## Utilizing the Split Window Feature
 
For convenience, you can open the lab guide in a separate window by selecting the **Split Window** button from the Top right corner.
 
   ![](media/labguide-1-1.png)
 
## Managing Your Virtual Machine
 
Feel free to start, stop, or restart your virtual machine as needed from the **Resources** tab. Your experience is in your hands!
 
  ![](media/res-1.png)

## Lab Guide Zoom In/Zoom Out
 
To adjust the zoom level for the environment page, click the **A↕ : 100%** icon located next to the timer in the lab environment.

   ![](media/zoom-feature.png)

## Login to Azure Portal

1. In the JumpVM, click on the Azure portal shortcut of the Microsoft Edge browser from the desktop.

   ![](media/img-3.png "Lab Environment")

1. In the Welcome to Microsoft Edge page, select **Start without your data**, and on the help for importing Google browsing data page select **Continue without this data** button and proceed to select **Confirm and start browsing** on the next page.
   
1. On the **Sign in to Microsoft Azure** tab you will see a login screen, enter the following email/username and then click on **Next**. 
   * Email/Username: <inject key="AzureAdUserEmail"></inject>
   
     ![](media/image7.png "Enter Email")
     
1. Now enter the following password and click on **Sign in**.
   * Password: <inject key="AzureAdUserPassword"></inject>
   
     ![](media/image8.png "Enter Password")
     
1. If you see the pop-up **Stay Signed in?**, click No

1. If you see the pop-up **You have free Azure Advisor recommendations!**, close the window to continue the lab.

1. If a **Welcome to Microsoft Azure** popup window appears, click **Cancel** to skip the tour.
   
1. Now you will see the Azure Portal Dashboard, click on **Resource groups** from the Navigate panel to see the resource groups.

    ![](media/select-rg.png "Resource groups")
   
1. Confirm you have resource groups present as shown in the below screenshot. The last six digits in the resource group name are unique for every user.

    ![](media/openai-1.png "Resource groups")
   

This hands-on lab aims to empower participants in leveraging OpenAI technologies within Azure environments, spanning data ingestion, application development, prompt engineering, model optimization, and theoretical AI concepts for comprehensive learning and application.

## Support Contact
 
The CloudLabs support team is available 24/7, 365 days a year, via email and live chat to ensure seamless assistance at any time. We offer dedicated support channels tailored specifically for both learners and instructors, ensuring that all your needs are promptly and efficiently addressed.

Learner Support Contacts:
- Email Support: cloudlabs-support@spektrasystems.com
- Live Chat Support: https://cloudlabs.ai/labs-support

Now, click on **Next** from the lower right corner to move on to the next page.

### Happy Learning!!
