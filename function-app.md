# Step-by-Step Function App Deployment Manual

## Objective

The objective of this guide is to provide a clear, step-by-step approach to deploying Virtual Machines (VMs) efficiently and securely across various environments. It aims to equip IT professionals, system administrators, and DevOps engineers with the necessary knowledge and best practices to plan, configure, deploy, and manage VMs using automated and manual methods. This guide ensures consistency, scalability, and optimal performance in VM deployments, while aligning with organizational IT policies and cloud architecture standards.

## Task 1: Deployment of Function App

In this Exercise you will be deploying an Function App

1. On the **Azure portal**, click on search bar, search for **Function App** **(1)**, and select **Function App** **(2)**.

   ![Search Bar](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093318.png)

2. In the **Fucntion App** tab, click on **+ Create** **(1)**.

   ![Create Button]([image-16.png](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093300.png))

3. In the Create Function App tab select **Consumption** **(1)** and then click on **Select** **(2)**

   ![Hosting Option]([image-17.png](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093345.png))

4. In the Basics tab, fill the following details and click on **Next : Storage >** **(8)**:

   - Subscription : click on the drop down and select **Innova8 Training** **(1)**.
   - Resource Group : click on the drop down and select **your particular resource group** **(2)**.
   - Function App Name : give your function app a **unique name** **(3)**.
   - Operating System : select **Linux(legacy)** **(4)**.
   - Runtime Stack : click on the drop down and select **Python** **(5)**.
   - Version : click on the drop down and select **3.11** **(6)**.
   - Region : click on the drop down and select **West US** **(7)**.

   ![Basics Tab]([image-18.png](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093405.png))

5. In the Storage tab, fill the following and click on **Review  + Create** **(4)**.

   Storage Account : click on **Create new** **(1)** and give your storage account a **unique name** **(2)** and click on **OK** **(3)**.

   ![Storage Tab]([image-19.png](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093429.png))

6. In the Review + Create tab, click on **Create** **(1)**

   ![Create Button]([image-21.png](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093447.png))

7. You will be redirected to the **Microsoft.Web-FunctionApp-Portal** tab, click on **Go to resources** **(1)**

   ![Go To Resource]([image-24.png](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093507.png))

8. When you land on the overview tab, click on **Create function** **(1)**

   ![Create Function]([image-25.png](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093529.png))

9. A side panel will pop up with **Create funtion** containing **Select a template** tab, select **Blob trigger** **(1)** under that and click on **Next** **(2)**

   ![Select A Template]([image-26.png](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093548.png))

10. After clicking on next, under **Template details** fill the following details and click on **Create** **(6)**:

   - Provide a function name : give your function any **name** **(1)**.
   - Path : provide a path to your container **your_container_name/{name}** **(2)**.
   
<details>
<details>
  <summary>Note</summary>
  - Before specifying a path, ensure that you have created a container. To create a container, duplicate this tab and navigate to **Home**, then go to your **Resource Group** and select your **Newly created storage account**. In the side panel, under **Data storage**, click on **Containers** and then click on **+ Container** to create a new container. Give the container a name and click **Create**. **Do not close this tab** and ensure that the container name you use matches the one you enter in the **Path** field (**(2)**).
</details>

   - Storage account connection : click on **new** **(3)**, click on the drop down and select **your storage account** **(4)**, click on **OK** **(5)**

   ![Template Details]([image-27.png](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20100119.png))

11. Once the function is created, you'll be redirected to the **Code + Test** section. Wait until the **connection** **(1)** is established (as shown below), then navigate to the **Logs** **(2)** and wait for the **'Connected'** **(3)** message to appear."**

   ![alt text]([image-31.png](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093603.png))
   ![alt text]([image-29.png](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093619.png))

12. Now go to the dupliacted page and go to your newly created container and upload an image.
<details>
  <summary> Note</summary>

  To navigate to your container, Click on **your_container** that you have created, you can see an upload button, click on it and click on **browse files** and select any image from your file manager, click on **upload**
</details>

13. After uploading an image, come back to your Logs tab to see all the logs of your function (as shown below). 

   ![Function Logs](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093640.png)

You have now successfully delpolyed your Function App and created a function to see all the logs of your function.
