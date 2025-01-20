# Module 1 - Lab 1 - Explore Microsoft Defender XDR

## Lab scenario
 You are a Security Operations Analyst working at a company that is implementing Microsoft Defender XDR. You start by assigning preset security policies in EOP and Microsoft Defender XDR for Office 365.

## Lab objectives
In this lab, you will perform:
- Task 1: Create a Group in Microsoft Entra ID
- Task 2: Apply Microsoft Defender XDR for Office 365 present security policies
- Task 3: Preparing the Microsoft Defender XDR workspace
    
## Estimated timing: 60 minutes

## Architecture Diagram

  ![Picture 1](../Media/archdialab1.png)

### Task 1: Create a Group in Microsoft Entra ID

In this task, you will create a new group in Microsoft Entra ID using the Azure portal.

1. In the Search bar of the Azure portal, type **Microsoft Entra ID**, then select **Microsoft Entra ID**.

1. Select **Groups** and then click on **New group**.

1. Enter the below details for the new group page:

   |Setting|Value|
    |---|---|
    |Group Type| **Microsoft 365** (1)|
    |Group Name| **Sg-IT-<inject key="DeploymentID" enableCopy="false"/>** (2)|

   ![Picture 1](../Media/newgroup1.png)

1. Click on **No owners selected (1)** and select the **ODL_user <inject key="DeploymentID" enableCopy="false"/>** from the list and then click on **Select**.

   ![Picture 1](../Media/newgroup2.png)

1. Click on **No members selected** and select the **ODL_user <inject key="DeploymentID" enableCopy="false"/>** from the list and then click on **Select**.

   > **Note**: Make sure you have selected **Group type** as Microsoft 365.

1. Select **Create.(2)**

### Task 2: Apply Microsoft Defender XDR for Office 365 preset security policies

In this task, you will assign preset security policies for Exchange Online Protection (EOP) and Microsoft Defender XDR for Office 365 in the Microsoft  security portal.

1. In the Edge browser, go to the Microsoft  Defender XDR portal at (https://security.microsoft.com).

1. You'll see the Sign into Microsoft Defender XDR portal tab. Here, enter your credentials:
 
   - **Email/Username:** <inject key="AzureAdUserEmail"></inject>
 
       ![Enter Your Username](../Media/sc900-image-1.png)
 
1. Next, provide your password:
 
   - **Password:** <inject key="AzureAdUserPassword"></inject>
 
       ![Enter Your Password](../Media/sc900-image-2.png)

    >**Note:** If you receive a message "The operation could not be completed. Please try again later. If the problem persists, contact Microsoft support." Click **OK** to continue.

1. If shown, close the Microsoft Defender XDR quick tour.

1. From the navigation menu, under *Email & Collaboration* area, select **Policies & rules**.

1. On the *Policy & rules* dashboard, select **Threat policies**.

1. On the *Threat policies* dashboard, select **Preset Security Policies**.

    >**Note:** If you receive the message *"Client Error - An error occurred when retrieving preset security policies. Please try again later."* Select **OK** to continue. Refresh your browser using **Ctrl+F5**.

1. On the **Learn about preset security policies** *pop-out* page, select **Cancel**.

1. Under **Standard protection**, select **Manage protection settings**. **Hint:** If you see this option greyed out, refresh your browser using **Ctrl+F5**.

   ![Standart protection](../Media/std1protect.png)

    >**Note:** After clicking on **Manage protection settings**, This might need 40 to 60 Minutes to load the content, wait for 40 to 60 Minutes to load the page completely after 40 to 60 Minutes back to the same page and might need to sign out of Microsoft defender XDR and sign in again and then try repeating the steps again to move forward. 

1. In the *Apply Exchange Online Protection* page, select **Specific recipients** under **Apply protection to:** and under **Domains** you can see that your domain is selected, if not start writing your tenant's domain name, select it, and then select **Next**.

   ![Standart protection](../Media/stdprotect.png)
                                                                              
    >**Hint:** Your tenant's domain name is the same that you have for your admin account, it might be something like *mocholxxxxx.onmicrosoft.com*. Notice that this configuration applies policies for anti-spam, outbound spam filters, anti-malware, and anti-phishing. 

1. In the *Apply Defender for Office 365 protection* page, apply the same configuration as the previous step and select **Next**. Notice that this configuration applies policies for anti-phishing, Safe Attachments, and Safe Links.

1. In the *Impersonation protection* page, select **Next** for next all steps i.e. (4x times) to continue.

1. If a popup appears for *Policy mode* page, make sure the **Turn on the policy when finished** radio button is selected, and then select **Next**.

1. Read the content under *Review and confirm your changes* and select **Confirm** to apply the changes and then select **Done** to finish.

1. Under **Strict protection**, select **Manage protection settings**. **Hint:** *Strict protection* is found under "Email & Collaboration - Policies & rules - Threat policies - Preset security policies".

1. In the *Apply Exchange Online Protection* page, select **Specific recipients** and under **Groups** start writing **Sg-IT-<inject key="DeploymentID" enableCopy="false"/>**, select it, and then select **Next**. Notice that this configuration applies policies for anti-spam, outbound spam filters, anti-malware, and anti-phishing.

   >**Note**: If a group is already selected, make sure it is **Sg-IT-<inject key="DeploymentID" enableCopy="false"/>**. else, remove and add it.

1. In the *Apply protection to* page, apply the same configuration as the previous step and select **Next**. Notice that this configuration applies policies for anti-phishing, Safe Attachments, and Safe Links.

1. In the *Impersonation protection* page, select **Next** for next all steps i.e. (4x times) to continue.

1. In the *Policy mode* page, make sure the **Turn on the policy when finished** radio button is selected, and then select **Next**.

1. Read the content under *Review and confirm your changes* and select **Confirm** to apply the changes and then select **Done** to finish.

### Task 3: Preparing the Microsoft Defender XDR workspace

In this task, you will prepare the Microsoft Defender XDR workspace by setting up the required configurations.

1. On the **Microsoft Defender** portal, from the navigation menu, select **Home** from the left.

    >**Note:** You may need to scroll all the way to the menu top.

1. On the **Home** portal page, the **Get your SIEM and XDR in one place** banner is displayed.

1. Scroll down the menu items to **Assets** and select **Devices**.

1. The process to deploy the Defender XDR workspace should start and you should see messages saying *loading and Initializing* briefly displayed at the top of the page, and then you're going to see an image of a coffee mug and a message that reads: **Hang on! We're preparing new spaces for your data and connecting them.** It will take approximately 5 minutes to finish. *Leave the page open and make sure it finishes since it is required for the next Lab.*

   >**Note:** If the message "Hang on! We're preparing new spaces for your data and connecting them" does not appear, or the "Settings > Microsoft Defender XDR > Account" page opens, but you see the message "Failed to load data storage location. Please try again later", select "Alert service settings" from the "General" menu, or go to the navigation menu, scroll down to the "Assets" section and select "Devices".

1. When the new space is completed successfully, you will see the Microsoft Defender XDR General settings for Account, Email notifications, Alert service settings, Permissions and Roles, and Streaming API. You will also see **Preview Features** turned on.

   > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
   > - Hit the Validate button for the corresponding task. You can proceed to the next task if you receive a success message.
   > - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
   > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help you out.

   <validation step="cd91c5ce-77b6-4769-8216-ebe3792185a5" />

### Review
 In this lab, you have completed the following:
   - Created a Group in Microsoft Entra ID
   - Applied Microsoft Defender XDR for Office 365 preset security policies
   - Prepared the Microsoft Defender XDR workspace

## You have successfully completed the lab.
