# Lab 07: Connect Defender XDR to Microsoft Sentinel using data connectors

## Estimated Duration: 40 minutes

## Lab scenario

![Lab overview.](../Media/23-05-2024.png)

You're a Security Operations Analyst working at a company that deployed both Microsoft Defender XDR and Microsoft Sentinel. You need to prepare for the Unified Security Operations Platform connecting Microsoft Sentinel to Defender XDR. Your next step will be to install the Defender XDR Content Hub solution and deploy the Defender XDR data connector to Microsoft Sentinel.

>**Important:** Be aware that there are capability differences between the azure Microsoft Sentinel portal and Sentinel in the Microsoft Defender XDR portal **[Portal capability differences](https://learn.microsoft.com/azure/sentinel/microsoft-sentinel-defender-portal#capability-differences-between-portals)**.

## Lab Objectives

- Task 1: Connect Defender XDR

### Task 1: Connect Defender XDR

In this task, you deploy the Microsoft Defender XDR connector.

1. Login to WIN1 virtual machine as Admin with the password: **Pa55w.rd**.  

1. In the Microsoft Edge browser, navigate to the Azure portal at (<https://portal.azure.com>).

1. In the **Sign in** dialog box, copy, and paste in the **Tenant Email** account provided by your lab hosting provider and then select **Next**.

1. In the **Enter password** dialog box, copy, and paste in the **Tenant Password** provided by your lab hosting provider and then select **Sign in**.

1. In the Search bar of the Azure portal, type *Sentinel*, then select **Microsoft Sentinel**.

1. Select the Microsoft Sentinel Workspace you created earlier.

1. In the Microsoft Sentinel left menus, scroll down to the **Content management** section and select **Content Hub**.

1. In the *Content hub*, search for the **Microsoft Defender XDR** solution and select it from the list.

1. On the *Microsoft Defender XDR* solution details page, select **Install**.

1. When the installation completes,  search for the **Microsoft Defender XDR** solution and select it.

1. On the *Microsoft Defender XDR* solution details page, select **Manage**

    >**Note:** The *Microsoft Defender XDR* solution installs the *Microsoft Defender XDR* Data connector, Hunting queries, Workbooks and Analytics rules.

1. Select the *Microsoft Defender XDR* Data connector check-box, and select **Open connector page**.

1. In the *Configuration* section, under the *Instructions* tab, **select** the checkbox for *Turn off all Microsoft incident creation rules for these products. Recommended*, and select the **Connect incidents & alerts** button.

    >**Note:** If you are not able to see the **Connect incident & alerts button**, Follow the following steps:
    >- Search for **Microsoft Defender For Cloud** in the azure portal and **Select** it, in the **Getting started** page Select **Upgrade** to upgrade your Microsoft Defender For cloud plan.
    >- Go to **Environment Settings** under **Management** and select your subscription.
    >- GO to **Defender plans** and click on **settings** under **Partial** in **Defender CSPM**.
    >- Turn **ON** the option next to **Permission Management (CIEM)** and click on **Continue** on top of the page.
    >- Click on **Save** on the **Settings | Defender Plans** page.

    >**Note:** If you are not able to see the **Connect Incident & alrets button**, wait for some time. It might take 25-30 minutes to show.

1. You should see a message that the connection was successful.

### Task 2: Connect Microsoft Sentinel and Microsoft Defender XDR

In this task, you'll connect a Microsoft Sentinel workspace to Microsoft Defender XDR.

>**Note:** Microsoft Sentinel in the Microsoft Defender XDR portal is in public preview and the user interface experience and steps may differ from the lab instructions.

1. Log in to the **WIN1** virtual machine as *Admin* with the password: **Pa55w.rd**.  

1. Start the Microsoft Edge browser.

1. In the Edge browser, go to the Microsoft Defender XDR portal at (https://security.microsoft.com).

1. In the **Sign in** dialog box, copy, and paste in the tenant Email account for the admin username provided by your lab hosting provider and then select **Next**.

1. In the **Enter password** dialog box, copy, and paste in the admin's tenant password provided by your lab hosting provider and then select **Sign in**.

    >**Tip:** The admin's tenant email account and password can be found on the Resources tab.

1. On the **Defender XDR** portal **Home** screen, you should see a banner at the top with the message, *Get your SIEM and XDR in one place*. Select the **Connect a workspaces** button.

   >**Note:** If the options are not visible, please wait 40 to 60 minutes for them to appear in the Defender portal. After this time, return to the same page. You may need to sign out of Microsoft Defender XDR, sign back in, and then repeat the steps to proceed.

1. On the *Choose a workspace* page, select the **Microsoft Sentinel** workspace you created earlier.

    >**Hint:** It should have a name like *uniquenameDefender*.

1. Select the **Next** button.

    >**Note:** If the *Next* button is disabled or greyed out, and you see an error message that the Microsoft Sentinel workspace is *not onboarded* to Defender XDR, try refreshing the Defender XDR portal page as it may take 5 to 10 minutes to sync up.

1. On the *Review changes* page, verify that the *Workspace* selection is correct and review the bulleted items under the *What to expect when the workspace is connected* section. Select the **Connect** button.

1. You should see a *Connecting the workspace* message followed by a *Workspace successfully connected* message.

1. Select the **Close** button. 

1. On the **Defender XDR** portal **Home** screen, you should see a banner at the top with the message, *Your unified SIEM and XDR is ready*. Select the **Start Hunting** button.

1. In *Advanced hunting*, you should see a message to "Explore your content from Sentinel". In the left menu pane, note the *Microsoft Sentinel* tables, functions, and queries under the corresponding tabs.

1. Expand the left main menu pane if collapsed and  expand the new **Microsoft Sentinel** menu items. You should see *Threat management*, *Content management* and *Configuration* selections.

 >**Note:** Some features may not be available in the public preview, and the user interface may differ from the lab instructions. Also, the synchronization between Microsoft Sentinel and Microsoft Defender XDR may take a few minutes to complete, so you may not see all the installed *Data connectors* for example.

## Summary

In this lab, you have connected Defender XDR.

## You have successfully completed the lab!
