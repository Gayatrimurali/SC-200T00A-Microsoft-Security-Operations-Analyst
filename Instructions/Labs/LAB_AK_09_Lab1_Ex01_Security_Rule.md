# Module 9 - Lab 1 - Exercise 1 - Modify a Microsoft Security rule

## Lab scenario

You are a Security Operations Analyst working at a company that implemented Microsoft Sentinel. You must learn how to detect and mitigate threats using Microsoft Sentinel. First, you need to filter the alerts coming from Defender for Cloud into Microsoft Sentinel, by Severity. 

>**Note:** An **[interactive lab simulation](https://mslabs.cloudguides.com/guides/SC-200%20Lab%20Simulation%20-%20Modify%20a%20Microsoft%20Security%20rule)** is available that allows you to click through this lab at your own pace. You may find slight differences between the interactive simulation and the hosted lab, but the core concepts and ideas being demonstrated are the same.

>**Important:** The lab exercises for Learning Path #9 are in a *standalone* environment. If you exit the lab before completing it, you will be required to re-run the configurations again.

## Lab objectives

 In this lab, you will perform the following:
 - Task 1: Activate a Microsoft Security Rule

## Estimated timing: 20 minutes

## Architecture Diagram

  ![Lab overview.](../Media/SC200-Lab_Diagrams_Mod7_L1_Ex1upd.png)

### Task 1: Activate a Microsoft Security Rule

In this task, you will activate a Microsoft Security rule.

1. In the Search bar of the Azure portal, type **microsoft sentinel**, then select **Microsoft Sentinel**.

1. Select your Microsoft Sentinel Workspace that you created in the previous lab.
        
1. Select **Analytics** from the Configuration area. By default, you will see the *Active rules*.

1. Select the **+ Create** button from the command bar and select the **Microsoft incident creation rule**.

1. Under Name, enter **Create incidents based on Defender for Endpoint**.

1. Scroll down and under Microsoft security service select **Microsoft Defender for Endpoint**. 

1. Under Filter by Severity, select the **Custom** option select Low, Medium, and High for the severity level.

1. Select the **Next: Automated response** button and then select **Next: Review + create** button.

1. Click on **save**.

### Review
In this lab, you have successfully activated a Microsoft Security Rule.

## Select **Next** to continue to Lab 2.
