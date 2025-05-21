# Step-by-Step App Service Deployment Guide

## Objective of the Lab

- Deploy a **Web App** using Azure App Service.
- Learn how to configure App Service settings including runtime, region, and deployment options.
- Integrate GitHub for continuous deployment.
- Gain hands-on experience managing web applications in a cloud environment.

---

## Task 1: Deploying a Web App in Azure App Service

In this task, you will deploy a Java-based Web App on Azure using App Service and configure it for continuous deployment from GitHub.

---

### Step 1: Navigate to App Service

1. In the **Azure portal**, type **App Service** into the search bar **(1)**.
2. Select **App Service** from the search results **(2)**.

   ![image](https://github.com/user-attachments/assets/bef7f2fe-6100-4500-9223-4289574ad29c)

---

### Step 2: Start Creating a Web App

1. On the App Service page, click **+ Create** **(1)**.
2. From the dropdown, select **Web App** **(2)**.

   ![image](https://github.com/user-attachments/assets/7c548b63-4e68-488a-a89d-c18e33b0dc61)

---

### Step 3: Fill in the Basics Tab

In the **Basics** tab, enter the following details:

- **Subscription**: Choose **Innova8 Training** **(1)**.
- **Resource Group**: Select your existing resource group **(2)**.
- **Name**: Provide a unique name for your web app **(3)**.
- **Publish**: Select **Code** **(4)**.

   ![image](https://github.com/user-attachments/assets/6158948f-4414-41e0-97ac-504f6186d372)

- **Runtime Stack**: Select **Java 17** **(1)**.
- **Java Web Server Stack**: Choose **Java SE (Embedded Web Server)** **(2)**.
- **Operating System**: Select **Windows** **(3)**.
- **Region**: Choose **West US** **(4)**.

- **Windows Plan**:
  - Click **Create new**, enter a name for your App Service plan, and click **OK** **(5)**.
  - Click **Next: Database >** to continue **(6)**.

   ![image](https://github.com/user-attachments/assets/1096353b-c91e-4e0b-b25a-e9a2ca6e3b43)

---

### Step 4: Skip the Database Tab

- No database is needed for this web app.
- Simply click **Next: Deployment** **(1)**.

   ![image](https://github.com/user-attachments/assets/51ae64b2-5542-471c-91ca-becef2ab97ba)

---

### Step 5: Configure Deployment Settings

1. In the **Deployment** tab:
   - **Continuous Deployment**: Enable it **(1)**.
   - **GitHub Account**: Click **Change account** **(2)**.
     - A popup will appear — authorize **AzureAppServices**, enter your GitHub password, and click **Confirm**.

2. Fill the remaining fields:
   - **Organization**: Enter your GitHub username **(3)**.
   - **Repository**: Select the repository where your code is stored **(4)**.
   - **Branch**: Select **main** **(5)**.

3. Click **Review + create** **(6)**.

   ![image](https://github.com/user-attachments/assets/ab75e88b-5a9f-419f-a88e-088f5859d83e)

   ![image](https://github.com/user-attachments/assets/88fa5cd1-e52a-4ae9-94c4-e25004baaa8b)

   ![image](https://github.com/user-attachments/assets/1f2f7036-28de-4997-a927-c3c10b5fbf07)

---

### Step 6: Create the App Service

- On the **Review + create** page, verify all configurations.
- Click **Create** **(1)** to begin deployment.

   ![image](https://github.com/user-attachments/assets/16060858-f659-4d8e-86cf-1a5dbe2f711f)

---

### Step 7: Access the Deployed Web App

1. Once deployment is complete, click **Go to resource** **(1)** on the deployment page.

   ![image](https://github.com/user-attachments/assets/9d4e0b75-8a4f-4303-9d9d-27c876dc9304)

2. In the **Overview** tab of your App Service, click **Browse** **(1)** to open your live web application.

   ![image](https://github.com/user-attachments/assets/920bea46-91bf-48fc-a90f-e921307b3ab1)

---

## ✅ You have successfully deployed a Java-based Web App on Azure App Service!
