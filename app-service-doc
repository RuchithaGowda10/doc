
# Exercise 1: Create App Service Plan & Web App
Azure App Service is a fully managed Platform-as-a-Service (PaaS) offering from Microsoft Azure that enables you to:
- Deploy web apps (ASP.NET, Node.js, Python, Java, PHP, static sites)
- Scale automatically based on demand
- Secure with built-in HTTPS, authentication, and compliance
- Integrate with databases, APIs, and DevOps pipelines

### **Task 1: Create a App Service**
1. Search for "App Services" In the Azure Portal top search bar, type "App Services" and select it from the dropdown.
   ![](Images/22.png)

1. Click + "Create" On the App Services page, click the + "Create" button, Select "Web App" Choose "Web App" from the creation options.
   ![](Images/7.png)  

1. Subscription & Resource Group : Select the Subscription innov8 and Resource Group: Select the pre-created lab RG (e.g., chandra.shekar1999-RG). Name Your Web App Enter a globally unique name (e.g., webapp-[yourinitials]-001). Runtime Stack Publish: Code (default) Runtime stack: Select Node.js 18 LTS (or your lab’s specified stack).
Note: Azure will validate availability with a green checkmark.
   ![](Images/8.png)

1. Operating System : Select Linux (or Windows if specified in lab).Region : Choose the region closest to you (e.g., West US). And Create a New Linux Plan and the prizing plan as Primium V3 POV3 to perform. And Click on for Next Database for the Next Step.
   ![](Images/9.png)
   
1. In the Create a Database Option No need to click on create a database Option leave it as default and go for the deployment section
   ![](Images/10.png)
   

1. Now, In the continuous Deployment section : Enable the Deployment section and after that Set up GitHub Actions to push content to your app whenever there are code changes made to your repository. Note: Your GitHub account must have write access to the selected repository in order to add a workflow file which manages deployments to your app.
- Give the github account Details
- Enter your Github organization Details
- Select the repository which you have stored your script
- Select the branch (Ex: main bracnch/Feature Branch)
Now Click on next and Go for the networking part
   ![](Images/11.png)
  

1. In the networking Part Make the Enable the Public access on When you enable public access, you're allowing the app to be accessible over the internet using a public URL like:https://yourappname.azurewebsites.net and Leave the Enable Virtual Network Integration as Default
   ![](Images/12.png)

1. Here Enable the Application Insights and create a New insight and It will automatically select the Region and Now Click on Review+Create 
   ![](Images/13.png)

1. After clicking on review + Create, The Deployment will be taking Place as shown In figure Wait for the Deployment to complete
   ![](Images/14.png)

1. Once the Deployment is Complete Your Home page will show Like Below Image.Now Go for Next Step
   ![](Images/15.png)

### **Task 2: Create and Set Up App Service Plan**
App Service plans give you the flexibility to allocate specific apps to a given set of resources and further optimize your Azure resource utilization. This way, if you want to save money on your testing environment you can share a plan across multiple apps.

1. Create New App Service Plan Click "Create new" under App Service Plan. Plan Name Enter a name (e.g., ASP-SpektraLab-001).
   ![](Images/16.png)

1. Select the Subcription and resource group and enter the name as App service and select the region as west US
   ![](Images/17.png)

1. Now select the Prizing plan as Premium V3 P1V3 and select review+Create
   ![](Images/18.png)

1. So the Deployment will be completed as shown in figure and Wait for the green "Deployment complete" notification (~1-2 mins)
   ![](Images/19.png)

### **Task 3: Access Your Web App**
1. Go to Resource Click "Go to resource" post-deployment. Test Default Page Under the "Overview" tab, click the URL (e.g., https://webapp-[yourinitials]-001.azurewebsites.net). A default "Your App Service app is up and running" page should load as shown in figure below.
   ![](Images/20.png)
   ![](Images/21.png)  
