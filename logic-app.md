# Step-by-Step Logic App Deployment Manual

## Objective

The objective of this guide is to provide a clear, step-by-step approach to deploying Virtual Machines (VMs) efficiently and securely across various environments. It aims to equip IT professionals, system administrators, and DevOps engineers with the necessary knowledge and best practices to plan, configure, deploy, and manage VMs using automated and manual methods. This guide ensures consistency, scalability, and optimal performance in VM deployments, while aligning with organizational IT policies and cloud architecture standards.

## Task 1: Deplyment of Logic App

In this Ex you will be deploying an Logic App

1. On the **Azure portal**, click on search bar, search for **Logic App** **(1)**, and select **Logic App** **(2)**.

   ![image](https://github.com/user-attachments/assets/13e8dfea-9a43-49df-a410-684693690887)

2. In the **Logic App** tab, click on **+ Add** **(1)**.

   ![image](https://github.com/user-attachments/assets/39241823-860b-4275-afe0-df048641b72a)

3. In the Create Logic App tab click on **Workflow Service Plan** **(1)** under Standard, then click on **Select** **(2)**.

   ![image](https://github.com/user-attachments/assets/c047edaf-26f4-46ab-b8d6-481259986d86)

4. In the Basics Tab, fill the following details :

    - Subscription : Choose Innova8 Training. **(1)**
    - Resource Group : Select your particular Resource Group. **(2)**
    - Logic App name : Provide a name to your Logic App **(3)**
    - Region : Select **West Europe** **(4)**
    - Windows Plan : Click on **Create new** **(5)** and provide a **name for your windows plan** **(6)** and click on **OK** **(7)**.
      Once done click on **Next : Storage >** **(8)**
      
    ![image](https://github.com/user-attachments/assets/7252568d-b128-4bcb-8cd7-b012ba64c633)

5. Under the Storage tab:

   - Storage Type : Select **Azure Storage** **(1)**.
   - Storage account : click **Create new** **(2)**, provide a unique **name** **(3)**, and click **OK** **(4)**.
     Once done click on **Review + Create** **(5)**.
     
   ![image](https://github.com/user-attachments/assets/c3d08cb6-43d7-4145-a3ff-a40bf2dbb0d7)

6. Once your configurations are validated, click **Create** **(1)** under Reveiw + Create tab to deploy the Logic app:
   
    ![image](https://github.com/user-attachments/assets/c689aa58-f719-4352-bbb2-f0512c322486)

7. Once the deployment is complete, you will be redirected to Microsoft.Web-LogicApp-Portal tab, click on **Go to resource** **(1)**:
   
    ![image](https://github.com/user-attachments/assets/2a669584-b88f-4b75-9abf-9b92327f9251)

8. In the Overview blade, click **Create workflow** **(1)** to begin the process of adding a new workflow.
   
    ![image](https://github.com/user-attachments/assets/c352682c-59b7-4852-b08c-e8ec3a8bec42)

10. Under the workflows, click on **+ Add** **(1)** and again under that click on **Add** **(2)**:
    
    ![image](https://github.com/user-attachments/assets/00b71a87-75b4-40c9-8a79-cca2b9315c5f)

11. Under the New workflow blade, create your workflow by providing your **Workflow Name** **(1)** and select the State type as **Stateful** **(2)**, once done click on **Create** **(3)**:

    ![image](https://github.com/user-attachments/assets/41cb6c04-1e41-426d-b55c-e69e8bd49034)

12. Locate the workflow you created using its **name** **(1)**, then click to open it:

    ![image](https://github.com/user-attachments/assets/8c953ac5-3d0e-4778-a633-569e06b1f8ce)

13. You should now see an **"Add a trigger"** **(1)** option, click on it:

    ![image](https://github.com/user-attachments/assets/97684fa8-7395-44da-9eed-23117e41f347)

14. In the Add a trigger blade, on the search bar, search for **"when a http request is recieved"** **(1)** and select the **when a http request is recieved** **(2)** under Request:

    ![image](https://github.com/user-attachments/assets/d7ccb5d2-d712-493b-9af2-012c2a42b665)

15. After adding the http trigger, click on the **+** symbol, you will see an **Add an action** **(1)** option, click on it:

      ![image](https://github.com/user-attachments/assets/85ec1e44-b1b0-4532-a88e-e79c8d7f7191)

16. In the Add an action blade, search for **"outlook.com"** **(1)**, under that select **Send an email (V2)** **(2)**:

      ![image](https://github.com/user-attachments/assets/df7d08cc-0348-451f-9be2-3037bbb94a08)

17. Set the parameters:

    - To : Enter any **email address** **1**.
    - Specify the email subject and body **(2)**.

      ![image](https://github.com/user-attachments/assets/c28a95f6-b575-4288-9dd5-095632fc6fb3)

18. Click on the **Save** **1** button and click on **Run** **(2)**.
    
      ![image](https://github.com/user-attachments/assets/9f3bb305-1864-4be1-9e95-1e5a05342bb4)

20. Under your workflow blade, select **Run history** **(1)**:
    
      ![image](https://github.com/user-attachments/assets/4f032d84-0f23-46d6-8a81-0de1c2c60990)

21. Review your run history:

      ![image](https://github.com/user-attachments/assets/cae88ebb-3313-41ce-af98-53b33abe13c8)




      


