# **Step-by-Step Function App Deployment Manual**

## **Objective**

This guide aims to provide a comprehensive, step-by-step methodology for deploying Virtual Machines (VMs) with efficiency and security across multiple environments. It is designed to empower IT professionals, system administrators, and DevOps engineers with the knowledge and best practices required for planning, configuring, deploying, and managing VMs using both automated and manual techniques. The focus is on ensuring consistency, scalability, and optimal performance in VM deployments, all while adhering to organizational IT policies and cloud architecture standards.

## **Task 1: Deploying a Function App**

In this exercise, you will deploy a **Function App** in Azure.

### 1. **Search for and Select Function App**

   - On the **Azure portal**, type **Function App** in the search bar and select **Function App** from the results.

   ![Search Bar](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093318.png)

### 2. **Create a New Function App**

   - In the **Function App** tab, click on **+ Create** to initiate the configuration process.

   ![Create Button](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093300.png)

### 3. **Select Hosting Plan**

   - In the **Create Function App** tab, select the **Consumption** plan and click **Select**.

   ![Hosting Option](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093345.png)

### 4. **Fill in Basic Information**

   In the **Basics** tab, complete the following fields and click **Next: Storage >**:

   - **Subscription**: Choose **Innova8 Training**.
   - **Resource Group**: Select your **specific resource group**.
   - **Function App Name**: Enter a **unique name** for your function app.
   - **Operating System**: Choose **Linux (legacy)**.
   - **Runtime Stack**: Select **Python**.
   - **Version**: Choose **3.11**.
   - **Region**: Select **West US**.

   ![Basics Tab](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093405.png)

### 5. **Configure Storage**

   In the **Storage** tab, complete the following details:

   - **Storage Account**: Click **Create new**, provide a **unique name** for your storage account, and click **OK**.

   Once done, click **Review + Create**.

   ![Storage Tab](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093429.png)

### 6. **Review and Create the Function App**

   - Once your configurations are validated, click **Create** to deploy the function app.

   ![Create Button](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093447.png)

### 7. **Access the Newly Created Function App**

   - Once the deployment is complete, you will be redirected to the **Microsoft.Web-FunctionApp-Portal**. Click **Go to resource**.

   ![Go to Resource](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093507.png)

### 8. **Create a New Function**

   - In the **Overview** tab, click **Create function** to begin the process of adding a new function.

   ![Create Function](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093529.png)

### 9. **Select a Template for the Function**

   - In the side panel that appears, under **Select a template**, choose **Blob trigger** and then click **Next**.

   ![Select A Template](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093548.png)

### 10. **Configure Template Details**

   Under **Template details**, complete the following fields and click **Create**:

   - **Function Name**: Provide a name for your function.
   - **Path**: Enter a path to your container in the format `your_container_name/{name}`.

> **Note**: Before specifying a path, ensure that you have already created a container. To do so, duplicate this browser tab and go to **Home** > **Your Resource Group** > **Your newly created storage account**. Under **Data storage**, select **Containers** and click **+ Container**. Give your container a name and click **Create**. Return to the previous tab and enter the container's name in the **Path** field.

   - **Storage Account Connection**: Click **new**, select your **storage account**, and click **OK**.

   ![Template Details](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20100119.png)

### 11. **Monitor Function Logs**

   Once the function is created, navigate to the **Code + Test** section. Wait until the connection is established, then go to the **Logs** tab to view the connection status.

   ![Logs](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093603.png)
   ![Logs](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093619.png)

### 12. **Upload an Image to Trigger the Function**

   In the duplicate browser tab, go to your newly created container and upload an image:

   - Click on the **Upload** button, select **Browse files**, choose an image from your file manager, and click **Upload**.

### 13. **Verify the Function Execution**

   Return to the **Logs** tab to verify the logs of your function. You should see logs related to the uploaded image, confirming the function was triggered.

   ![Function Logs](https://raw.githubusercontent.com/RuchithaGowda10/doc-on-vm-creation/refs/heads/main/images/Screenshot%202025-05-05%20093640.png)

---

### **Conclusion**

You have now successfully deployed a **Function App** and created a function that logs actions triggered by image uploads. This exercise demonstrates the key steps in deploying and managing Function Apps within Azure.

---

