# Step-by-Step Logic App Deployment Guide

## Objective of the Lab

- Deploy a Logic App in Azure.
- Learn how to create and configure workflows using Azure Logic Apps.
- Automate processes like sending emails triggered by HTTP requests.
- Gain practical experience in managing workflows and integrating with external services like Outlook in a cloud environment.

## Task 1: Deploying a Logic App

In this exercise, you will be deploying a Logic App in Azure.

1. In the **Azure portal**, type **Logic App** into the search bar **(1)**, and then select **Logic App** from the results **(2)**.

   ![image](https://github.com/user-attachments/assets/13e8dfea-9a43-49df-a410-684693690887)

2. On the **Logic App** page, click **+ Add** **(1)** to create a new Logic App.

   ![image](https://github.com/user-attachments/assets/39241823-860b-4275-afe0-df048641b72a)

3. In the **Create Logic App** tab, select **Workflow Service Plan** under the **Standard** option **(1)**, and then click **Select** **(2)**.

   ![image](https://github.com/user-attachments/assets/c047edaf-26f4-46ab-b8d6-481259986d86)

4. In the **Basics** tab, complete the following fields:

    - **Subscription**: Choose **Innova8 Training** **(1)**.
    - **Resource Group**: Select your specific Resource Group **(2)**.
    - **Logic App Name**: Enter a unique name for your Logic App **(3)**.
    - **Region**: Choose **West Europe** **(4)**.
    - **Windows Plan**: Click **Create new** **(5)**, provide a **name for your Windows plan** **(6)**, and click **OK** **(7)**.
      Once finished, click **Next: Storage >** **(8)**.
      
      ![image](https://github.com/user-attachments/assets/7252568d-b128-4bcb-8cd7-b012ba64c633)

5. Under the **Storage** tab:

   - **Storage Type**: Select **Azure Storage** **(1)**.
   - **Storage Account**: Click **Create new** **(2)**, enter a unique **name** **(3)**, and click **OK** **(4)**.
     Once done, click **Review + Create** **(5)**.
     
     ![image](https://github.com/user-attachments/assets/c3d08cb6-43d7-4145-a3ff-a40bf2dbb0d7)

6. After your configuration is validated, click **Create** **(1)** under the **Review + Create** tab to deploy the Logic App.
   
    ![image](https://github.com/user-attachments/assets/c689aa58-f719-4352-bbb2-f0512c322486)

7. Once deployment is complete, you will be redirected to the **Microsoft.Web-LogicApp-Portal** page. Click on **Go to resource** **(1)** to access the resource.
   
    ![image](https://github.com/user-attachments/assets/2a669584-b88f-4b75-9abf-9b92327f9251)

8. In the **Overview** tab, click **Create workflow** **(1)** to begin creating a new workflow.

    ![image](https://github.com/user-attachments/assets/c352682c-59b7-4852-b08c-e8ec3a8bec42)

9. Under the **Workflows** section, click **+ Add** **(1)**, and then click **Add** again **(2)**.

    ![image](https://github.com/user-attachments/assets/00b71a87-75b4-40c9-8a79-cca2b9315c5f)

10. In the **New workflow** tab, create your workflow by entering a **Workflow Name** **(1)** and selecting the state type as **Stateful** **(2)**. Then, click **Create** **(3)**.

    ![image](https://github.com/user-attachments/assets/41cb6c04-1e41-426d-b55c-e69e8bd49034)

11. Find and click on the workflow you just created by its **name** **(1)**.

    ![image](https://github.com/user-attachments/assets/8c953ac5-3d0e-4778-a633-569e06b1f8ce)

12. You should now see an **"Add a trigger"** **(1)** option. Click on it.

    ![image](https://github.com/user-attachments/assets/97684fa8-7395-44da-9eed-23117e41f347)

13. In the **Add a trigger** tab, search for **"when a HTTP request is received"** **(1)** and select **when a HTTP request is received** under **Request** **(2)**.

    ![image](https://github.com/user-attachments/assets/d7ccb5d2-d712-493b-9af2-012c2a42b665)

14. After adding the HTTP trigger, click the **+** symbol to add a new action. You will see the **Add an action** **(1)** option. Click on it.

    ![image](https://github.com/user-attachments/assets/85ec1e44-b1b0-4532-a88e-e79c8d7f7191)

15. In the **Add an action** tab, search for **"outlook.com"** **(1)** and select **Send an email (V2)** **(2)**.
       > ⚠️ **Note**: You may be prompted to sign in with your Outlook/Microsoft account to authorize this connector.
       
       ![image](https://github.com/user-attachments/assets/df7d08cc-0348-451f-9be2-3037bbb94a08)

17. Set up the email action by providing the following parameters:

    - **To**: Enter any valid **email address** **(1)**.
    - **Subject** and **Body**: Specify the subject and body of the email **(2)**.
    
      ![image](https://github.com/user-attachments/assets/c28a95f6-b575-4288-9dd5-095632fc6fb3)

18. Click **Save** **(1)** and then click **Run** **(2)** to execute the workflow.

    ![image](https://github.com/user-attachments/assets/9f3bb305-1864-4be1-9e95-1e5a05342bb4)

19. In the **Workflow** tab, select **Run history** **(1)** to view the execution history.

    ![image](https://github.com/user-attachments/assets/4f032d84-0f23-46d6-8a81-0de1c2c60990)

20. Review the details of your workflow execution in the **Run history**.

    ![image](https://github.com/user-attachments/assets/cae88ebb-3313-41ce-af98-53b33abe13c8)

## Conclusion

Congrats on deploying your Logic App! You've successfully learned to automate tasks and create workflows in Azure.
