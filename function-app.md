# Step-by-Step Function App Deployment Manual

## Objective

The objective of this guide is to provide a clear, step-by-step approach to deploying Virtual Machines (VMs) efficiently and securely across various environments. It aims to equip IT professionals, system administrators, and DevOps engineers with the necessary knowledge and best practices to plan, configure, deploy, and manage VMs using automated and manual methods. This guide ensures consistency, scalability, and optimal performance in VM deployments, while aligning with organizational IT policies and cloud architecture standards.

## Task 1: Deployment of Function App

In this Exercise you will be deploying an Function App

1. On the **Azure portal**, click on search bar, search for **Function App** **(1)**, and select **Function App** **(2)**.

   ![alt text](image-15.png)

2. In the **Fucntion App** tab, click on **+ Create** **(1)**.

   ![alt text](image-16.png)

3. In the Create Function App tab select **Consumption** **(1)** and then click on **Select** **(2)**

   ![alt text](image-17.png)

4. In the Basics tab, fill the following details and click on **Next : Storage >** **(8)**:

   - Subscription : click on the drop down and select **Innova8 Training** **(1)**.
   - Resource Group : click on the drop down and select **your particular resource group** **(2)**.
   - Function App Name : give your function app a **unique name** **(3)**.
   - Operating System : select **Linux(legacy)** **(4)**.
   - Runtime Stack : click on the drop down and select **Python** **(5)**.
   - Version : click on the drop down and select **3.11** **(6)**.
   - Region : click on the drop down and select **West US** **(7)**.

   ![alt text](image-18.png)

5. In the Storage tab, fill the following and click on **Review  + Create** **(4)**.

   Storage Account : click on **Create new** **(1)** and give your storage account a **unique name** **(2)** and click on **OK** **(3)**.

   ![alt text](image-19.png)

6. In the Review + Create tab, click on **Create** **(1)**

   ![alt text](image-21.png)

7. You will be redirected to the **Microsoft.Web-FunctionApp-Portal** tab, click on **Go to resources** **(1)**

   ![alt text](image-24.png)

8. When you land on the overview tab, click on **Create function** **(1)**

   ![alt text](image-25.png)

9. A side panel will pop up with **Create funtion** containing **Select a template** tab, select **Blob trigger** **(1)** under that and click on **Next** **(2)**

   ![alt text](image-26.png)

10. After clicking on next, under **Template details** fill the following details and click on **Create** **(6)**:

   - Provide a function name : give your function any **name** **(1)**.
   - Path : provide a path to your container **your_container_name/{name}** **(2)**.
   
<details>
  <summary> Note</summary>
    Before providing a path, make sure you have created a container. (To create a container, go to **Home**, go to your **Resource Group**, select your **Newly created storage accout**, under the side panel go to **Data storage**, click on **Containers**, again click on **+ Container** to create new container, give your container a name and click on **Create** and make sure that is the same name you give in the **Path** **(2)**)
</details>
   - Storage account connection : click on **new** **(3)**, click on the drop down and select **your storage account** **(4)**, click on **OK** **(5)**

   ![alt text](image-27.png)

11. Once the function is created, you'll be redirected to the **Code + Test** section. Wait until the **connection** **(1)** is established (as shown below), then navigate to the **Logs** **(2)** and wait for the **'Connected'** **(3)** message to appear."**

   ![alt text](image-30.png)
   ![alt text](image-29.png)

12. Now dupliacte the tab and go to your container and upload an image.
<details>
  <summary> Note</summary>

  To navigate to your container, go to **Home**, go to your **Resource Group**, select your **Newly created storage accout**, under the side panel go to **Data storage**, click on **your_container** that you have created, you can see an upload button, click on it and click on **browse files** and select any image from your file manager, click on **upload**
</details>

13. After uploading an image, come back to your Logs tab to see all the logs of your function (as shown below). 

   ![alt text](image-31.png)

You have now successfully delpolyed your Function App and created a function to see all the logs of your function.
