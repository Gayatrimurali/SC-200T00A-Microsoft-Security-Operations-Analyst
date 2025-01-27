
# LAB PREREQUISITES

## Estimated timing: 40 minutes

## Prerequisites to be completed before proceeding to further exercises

### Prerequisite 01

### Task 1: Connect a non-Azure Windows Machine

In this task, you will install Azure Arc and connect a non-Azure Windows virtual machine to Microsoft Sentinel.  

   >**Important:** The next steps are done on a different machine than the one you were previously working on. Look for the Virtual Machine name references.

   >**Important:** The *Windows Security Events via AMA* data connector requires Azure Arc for non-Azure devices. 

1. In the lab virtual machine, Select **WINserver** from the desktop.

   ![Picture 1](../Media/46.png)

1. If **Connect to WINServer** prompted, click **Connect.**

     ![Picture 1](../Media/sc-200-3.png)  
    
1. Enter the **Password** as `Password.1!!` when prompted.

     ![Picture 1](../Media/sc-200-4.png)

1. Open the Microsoft Edge browser inside **WINSERVER**.

1. On your virtual machine, click on the Azure Portal icon as shown below:
 
     ![Launch Azure Portal](../Media/portal.png)
 
2. You'll see the **Sign into Microsoft Azure** tab. Here, enter your credentials:
 
   - **Email/Username:** <inject key="AzureAdUserEmail"></inject>
 
      ![Enter Your Username](../Media/AZ-500-siginazportal.png)
 
3. Next, provide your password:
 
   - **Password:** <inject key="AzureAdUserPassword"></inject>
 
     ![Enter Your Password](../Media/AZ-500-pass.png)

1. If you get a pop-up stating **Action Required** click on **Ask Later**.   
   
   ![](../Media/az500-2.png)
 
4. If prompted to stay signed in, you can click **No**.

    ![](../Media/AZ-500-staysignedin.png)
 
5. If a **Welcome to Microsoft Azure** pop-up window appears, simply click **Cancel** to skip the tour.

   >**Note:** If you are not able to copy-paste the username and password then:
   > - Go to Hyper-V manager.
   > - On the left-right click on **WINSERVER**.
   > - Click on Hyper-V settings.
   > - From there click on allow enhanced mode policy Under **Server** and enable the option.
   > - Again, click on allow enhanced mode under **User** and enable the option. Restart the WINSERVER machine once to reflect the changes.

   >**Note:** If the copy-paste functionality is still not working, copy the content that has to be pasted then from the top navigation pane of the WINSERVER Hyper-V VM click on **Clipboard** and choose **Type Clipboard text** to paste.
      
   > ![Picture 1](../Media/x0.png)

1. In the Search bar of the Azure portal, type *Arc*, then select **Azure Arc**.

     ![Picture 1](../Media/sc-200-5.png)

1. On the left side navigation pane under **Azure Arc Resources** select **Machines (1)** and then click on **+ Add/Create (2)** drop dowm and then click on **Add a Machine (3)**.

     ![Picture 1](../Media/sc-200-6.png)

1. Select **Generate script** in the **"Add a single server"** section.

     ![Picture 1](../Media/sc-200-7.png)

1. First, select the **East US** region.

1. Then, create a new resource group by clicking on **Create New (1)** with the name **RG-DEFENDER (2)** then click **OK (3)**

     ![Picture 1](../Media/sc-200-8.png)
     
1. Review the *Server details* and *Connectivity method* options. Keep the default values and select **Next** to get to the Tags tab.

     ![Picture 1](../Media/sc-200-9.png)

1. Select **Next** to get to the Download and run script tab.

1. Scroll down and select the **Download** button. **Hint:** If your browser blocks the download, take action in the browser to allow it. In Edge Browser, select the ellipsis button (...) if needed and then select **Keep**.

     ![Picture 1](../Media/sc-200-10.png)

1. Right-click the Windows Start button, In the search box type in **PowerShell**. You should see the **Windows PowerShell App** appear. Select the **Run as Administrator** option.

     ![Picture 1](../Media/sc-200-11.png)
   
1. In case you get a UAC prompt, enter *Administrator* for "Username" and *Passw0rd!* for "Password", else skip to the next step.

1. Enter: **cd C:\Users\Administrator\Downloads**

    >**Note:** If you are not able to copy the content, then copy the required content to a notepad file using the Clipboard functionality in the top navigation pane of the Hyper V VM in the lab VM and paste it into the Powershell window.
 
1. Type **Set-ExecutionPolicy -ExecutionPolicy Unrestricted** and press enter.

1. Enter **A** for Yes to All and press enter.

     ![Picture 1](../Media/sc-200-12.png)

1. Type **.\OnboardingScript.ps1** and press enter.  

    >**Important:** If you get the error *"The term .\OnboardingScript.ps1 is not recognized..."*, make sure you are doing the steps for Task 3 on the WINSERVER virtual machine. Another issue might be that the name of the file changed due to multiple downloads, search for *".\OnboardingScript (1).ps1"* or other file numbers in the running directory.

1. Enter **R** to Run once and press enter (this may take a couple of minutes).

     ![Picture 1](../Media/sc-200-13.png)

1. The setup process will open a new Edge browser tab to authenticate the Azure Arc agent. Select your admin account, wait for the message "Authentication complete" and then go back to the Windows PowerShell window.

     ![Picture 1](../Media/sc-200-14.png)

1. When the installation finishes,you will get a output like this in the powershell. 

     ![Picture 1](../Media/sc-200-15.png)

1. Then go back to the Azure portal page where you downloaded the script and select **Close**. Close the **Add servers with Azure Arc** to go back to the Azure Arc **Servers** page.

1. Select **Refresh** until **WIN-xxxxxxxxxxx** name appears.

    >**Note:** This could take a few minutes.

    >**Note:** **xxxxxxxxxxx** will be a random suffix of the **WIN-**, as demonstrated in the below image. 

     ![Picture 1](../Media/sc-200-16.png)
    
1. In the Azure portal's search bar, type **Log Analytics workspaces** and select it.

     ![Picture 1](../Media/sc-200-17.png)

1. Click on **+ Create**.

1. On the **Create Log Analytics workspace** provide the following details and click **Review + Create (4.)**

      - Subscription: Leave the default subscription **(1)**
      - Resource group: Select **RG-DEFENDER (2)**
      - Name: Enter  **uniquenameDefender (3)**

        ![Picture 1](../Media/sc-200-18.png)
        
1. Once the workspace validation has passed, select **Create**. Wait for the new workspace to be provisioned, this may take a few minutes.

1. In the Azure portal's search bar, type **Log Analytics workspaces** and Select the **uniquenameDefender (1)** you just created, click on **Virtual machines (deprecated) (3)** under **classic (3)** from the left panel, then select **WIN1 (4)** virtual machine.

   ![Picture 1](../Media/111.png)

1. On the WIN1 page, click on **Connect**.

   ![Picture 1](../Media/112.png)

1. Wait until its get connected.

   ![Picture 1](../Media/113.png)

1. In the Azure portal's search bar, type **Microsoft Sentinel** and select it.

     ![Picture 1](../Media/sc-200-19.png)

1. Click on **+ Create**.

1. Next, in Add Microsoft Sentinel to a workspace page select the existing workspace **(1)** that was created in the previous lab, then select **Add (2)**. This could take a few minutes.

     ![Picture 1](../Media/sc-200-20.png)

1. Select the Microsoft Sentinel Workspace you created.
 
1. Click on **Go to the content hub**, search for **Windows Security Events**, and click on **Install**.

     ![Picture 1](../Media/contenthub.png)
     ![Picture 1](../Media/installWSEvents.png)

1. Once the installation is completed, go to the data connector page and refresh you should find **Windows Security Events via AMA**.

     ![Picture 1](../Media/dataconnectors.png)

1. Select the **Windows Security Events via AMA** connector and click on **Open connector page** on the connector information blade. 

    >**Note:** You  may have to click on the arrowhead that appears to see the **Open Connector Page Option**

    ![Picture 1](../Media/m1.png)
 
1. In the **Configuration** section, select the **+Create data collection rule**.

     ![Picture 1](../Media/sc-200-21.png)

1. Enter **WINSERVER (1)** for Rule Name, then select **Next: Resources (2)**.

     ![Picture 1](../Media/sc-200-22.png)

1. Expand the **Subscription** and the **RG-DEFENDER** (or the Resource Group you have created), then select **WIN-xxxx**. Then select **Next: Collect** and **Next: Review + Create**.

     ![Picture 1](../Media/sc-200-23.png)

1. Select **Create**.

1. Wait a few minutes and then select **Refresh** to see the new data collection rule listed.

    > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
   - If you receive a success message, you can proceed to the next task.
   - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
   - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help you out.
 
   <validation step="07c96102-f314-44cd-b6a4-10fbb89a449b" />

**PROCEED TO  THE NEXT EXERCISE**
