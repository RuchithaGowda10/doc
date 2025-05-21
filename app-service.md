
# Step-by-Step App Service Deployment Guide

## Objective of the Lab

- Deploy a App Service in Azure.
- Learn how to create and configure workflows using Azure Logic Apps.
- Automate processes like sending emails triggered by HTTP requests.
- Gain practical experience in managing workflows and integrating with external services like Outlook in a cloud environment.

## Task 1: Deploying a App Service

In this exercise, you will be deploying a Logic App in Azure.

1. In the **Azure portal**, type **App Service** into the search bar **(1)**, and then select **App Service** from the results **(2)**.

   ![image](https://github.com/user-attachments/assets/bef7f2fe-6100-4500-9223-4289574ad29c)

2. On the App Service page, click **+ Create** **(1)** and from the drop down select **Web App** **(2)**

   ![image](https://github.com/user-attachments/assets/7c548b63-4e68-488a-a89d-c18e33b0dc61)

3. In the Basics tab, complete the following fields:

   Subscription: Choose Innova8 Training (1).

   Resource Group: Select your specific Resource Group (2).

   Name: Enter a unique name for your Wep app (3).

   Publish : select **code** **(4)**

   ![image](https://github.com/user-attachments/assets/6158948f-4414-41e0-97ac-504f6186d372)
   
   Runtime stack : **select Java 17**(1)

   Java web server stack : select **Java SE (Embedded Web Server)** **(2)**

   Operating System : select **Windows** **(3)**

   Region : select **WEST US** **(4)**


   Windows Plan: Click Create new, provide a name for your Windows plan, and click OK. **(5)** Once finished, click Next: Database > (6).

   ![image](https://github.com/user-attachments/assets/1096353b-c91e-4e0b-b25a-e9a2ca6e3b43)

4. Under database tab, move to **Next : Deployment** **1**
   ![image](https://github.com/user-attachments/assets/51ae64b2-5542-471c-91ca-becef2ab97ba)

5. Fill the following in deployment tab and click on **Review + create** **(6)**
   Continous deployment : **Enabled** **(1)**
   Github account : select **change account** **2**
   You will get a popup to link your github account, click on authorize azureappservices, provide your password and clcik on confirm.

   Organizaation : provide your **github account name** **(3)**
   Repository : provide your repo where the code has been stored **(4)**
   Branch : make sure it is **main** **(5)**

   ![image](https://github.com/user-attachments/assets/ab75e88b-5a9f-419f-a88e-088f5859d83e)
   
   ![image](https://github.com/user-attachments/assets/88fa5cd1-e52a-4ae9-94c4-e25004baaa8b)
   
   ![image](https://github.com/user-attachments/assets/1f2f7036-28de-4997-a927-c3c10b5fbf07)

   
7. Under Review + create tab, click on **Create** **(1)**
   ![image](https://github.com/user-attachments/assets/16060858-f659-4d8e-86cf-1a5dbe2f711f)

8. UNder the Microsoft.Web-WebApp-Portal, click on **Go to resources** **(1)**

   ![image](https://github.com/user-attachments/assets/9d4e0b75-8a4f-4303-9d9d-27c876dc9304)

9. Under the overview, you can see browse option, clcik on **Browse** **(1)** to be redirected to your web application. 

   ![image](https://github.com/user-attachments/assets/920bea46-91bf-48fc-a90f-e921307b3ab1)



