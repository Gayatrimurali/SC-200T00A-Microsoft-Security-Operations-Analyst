# Module 9 - Lab 1 - Exercise 4 - Explore Entity Behavior Analytics

## Lab scenario

You are a Security Operations Analyst working at a company that implemented Microsoft Sentinel. You already created Scheduled and Microsoft Security Analytics rules. 

You need to configure Microsoft Sentinel to perform Entity Behavior Analytics to discover anomalies and provide entity analytic pages.

>**Note:** An **[interactive lab simulation](https://mslabs.cloudguides.com/guides/SC-200%20Lab%20Simulation%20-%20Explore%20entity%20behavior%20analytics)** is available that allows you to click through this lab at your own pace. You may find slight differences between the interactive simulation and the hosted lab, but the core concepts and ideas being demonstrated are the same. 

## Lab objectives
 In this lab, you will perform the following:
- Task 1: Explore Entity Behavior 
- Task 2: Confirm and review Anomalies rules

## Estimated timing: 20 minutes

## Architecture Diagram

  ![Picture 1](../Media/archdialab9ex4.png)

### Task 1: Explore Entity Behavior 

In this task, you will explore Entity behavior analytics in Microsoft Sentinel.

1. In the Search bar of the Azure portal, type *Sentinel*, then select **Microsoft Sentinel**.

1. Select the Microsoft Sentinel Workspace you created earlier.

1. On the left menu Select the **Entity behavior** page.

1. On the popup from *Entity behavior settings*, select **Set UEBA**.

    ![Lab overview.](../Media/ueba.png)

1. On the *Settings* tab under *Entity behaviour analytics*, scroll down the *Anomalies* section and verify read through the paragraph, and verify that the *switch* is *On*.

1. Select the **Go to analytics in oder to configure the anomalies** link.

    ![Lab overview.](../Media/35.png)

### Task 2: Confirm and review Anomalies rules

In this task, you will confirm Anomalies analytics rules are enabled.

1. You should be now at the *Analytics* page, *Anomalies* tab.

1. Confirm status column of the rules is *Enabled*.

1. Select any rule and then select **Edit** on the rule blade (Select ellipsis (...) icon at the right of the rule to see the Edit option).

1. Review the *General* tab information. Notice the *Mode* is **Production** and then select **Next: Configuration**.

1. Review the *Configuration* tab information. Notice that you cannot change the **Anomaly score threshold**.

1. Then select **X** in the top right corner to exit the Analytics rule wizard.

1. Scroll right to the analytics rule you selected until see and select the ellipsis **(...)** icon.

1. Select **Duplicate** and scroll left to review the new rule with the **FLGT** tab at the beginning of the name.

1. Select **FLGT** rule and then select **Edit** on the rule blade.

     ![Lab overview.](../Media/flgt.png)

1. Review the *General* tab information. Notice the *Mode* is **Flighting** and then select **Next: Configuration**.

1. Review the *Configuration* tab information. Notice that you can now change the **Anomaly score threshold**.

1. Set the value to **1** and then select **Next: Submit Feedback**.

1. Select **Next: Review + Create** and then **Save** to update the rule.

    >**Note:** You can upgrade the **Flighting** rule to **Production** by changing the setting on this rule and saving the changes. The **Production** rule will become the **Flighting** rule afterward.
    
### Review
In this lab, you have understood the Attacks and Detection Modelling.

## Select **Next** to continue to Lab 5.
