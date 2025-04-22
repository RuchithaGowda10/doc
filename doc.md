## Step 1: Initiate Virtual Machine Creation

To begin the process of deploying a virtual machine in Azure, you'll first need to create a new resource.

1.  **Navigate to the Azure Services Menu**: This menu provides access to all of Azure's functionalities.
2.  **Click on the "+ Create a resource" Button**: This button, clearly highlighted in the red box in the screenshot, is the starting point for creating any new Azure resource, including virtual machines. Clicking this will take you to the Azure Marketplace, where you can select the type of resource you want to create.
![Screenshot 2025-04-22 113403](https://github.com/user-attachments/assets/fdd834b9-677a-488c-a3e4-15c45ba91b11)

## Step 2: Search for the Virtual Machine

After clicking "+ Create a resource," you will be directed to the Azure Marketplace. Here, you need to search for the specific resource you want to deploy, which in this case is a virtual machine.

1. **Locate the Search Bar**: This bar is typically at the top of the "Create a resource" page, as highlighted in the red box in the screenshot.
2. **Type "Virtual Machine" into the Search Bar**: As you type, you will likely see a dropdown menu appear with suggested search terms.
3. **Select "Virtual Machine" from the Search Results**: This will filter the Marketplace to show options related to creating virtual machines.
![Screenshot 2025-04-22 113420](https://github.com/user-attachments/assets/cb633543-b530-43e2-a03b-4aaced914d68)

## Step 3: Select the Virtual Machine

After searching for "virtual machine," you will see a list of various virtual machine offers available in the Azure Marketplace. These offers can differ based on the operating system, pre-installed software, and publisher.

1. **Identify the "Virtual machine"**: This is typically the first and most general option for creating a standard virtual machine, as highlighted in the red box in the screenshot. It is usually published by Microsoft and categorized under "Azure Service."
2. **Review the Description (Optional)**: The description below the "Virtual machine" offer provides a brief overview, stating that "Azure Virtual Machines provide on-demand, high-scale, secure, and virtualized infrastructure using either Linux or Windows operating systems."
3. **Click on the "Create" Button**: Located under your selected "Virtual machine", clicking this will initiate the configuration process for your new virtual machine.
![Screenshot 2025-04-22 113444](https://github.com/user-attachments/assets/bc09816f-50c9-44ee-9a4a-d0fab722a9cb)

## Step 4: Configure Basic Virtual Machine Settings (Basics Tab)

Once you've clicked **Create** on the Virtual Machine offer, you'll be directed to the **"Create a virtual machine"** page. Here, begin configuring your virtual machine under the **"Basics"** tab.

1. **Project Details**
- **Subscription**:  
  Select the Azure subscription you want to use. This determines billing and access control for the VM.

- **Resource Group**:  
  Choose an existing resource group or click **Create new** to define one.  
  Resource groups help logically organize your Azure resources.

2. **Instance Details**
- **Virtual Machine Name**:  
  Enter a unique name to identify your virtual machine.

- **Region**:  
  Select the Azure region where your VM will be hosted.  
  Choosing a region closer to your users helps reduce latency.  
![Screenshot 2025-04-22 113510](https://github.com/user-attachments/assets/196261a9-1e69-4819-93c7-30e92d60da3b)

- **Availability Options**:  
  Choose how Azure should provide infrastructure redundancy:
  - `No infrastructure redundancy required` (default)
  - `Availability zones`
  - `Availability sets`

- **Security Type**:  
  Select a security model (e.g., `Trusted launch virtual machines`).  
  For enhanced options, click **Configure security features**.

- **Image**:  
  Pick an OS image from the Azure Marketplace.  
  You can click **See all images** to explore more options.  
  Also configure VM generation (Gen1 or Gen2) if required.

- **VM Architecture**:  
  Choose processor architecture.  
  Azure will notify you if your selected image doesn’t support alternate architecture types like Arm64.

- **Run with Azure Spot Discount** (Optional):  
  Enable this option to use unused Azure capacity at a lower price.  
  Note: Spot VMs can be evicted at any time.

- **VM Size**:  
  Select the VM size according to your workload needs.  
  Click **See all sizes** to view full options.
![Screenshot 2025-04-22 113523](https://github.com/user-attachments/assets/b667b42d-7660-4c77-b640-8f964f4271fb)
  
3. **Administrator Account**
- **Username**:  
  Create a unique username to log in to your VM.

- **Password**:  
  Enter and confirm a strong password.  
  > ⚠️ Save these credentials securely. You’ll need them to access your virtual machine.

4. **Inbound Port Rules**
- **Public Inbound Ports**:  
  Choose the level of access from the internet:
  - `None` – Denies public access
  - `Allow selected ports` – Open specific ports (e.g., 22 for SSH, 3389 for RDP)

- **Select Inbound Ports**:  
  If allowing public access, select the ports you want to open.

5. **Licensing**
- Depending on the image selected, this section allows you to indicate if you're bringing your own license (e.g., for Windows Server).

![Screenshot 2025-04-22 113540](https://github.com/user-attachments/assets/9a92fe0f-a80e-4c4f-84af-99a919360fd7)

Once you're done filling out all the required fields, click the **"Next: Disks >"** button to move to the disk configuration step.

## Step 5: Configure Disks

In this step, you configure the **Operating System (OS) disk** and any additional **data disks** that your virtual machine will use.

1. VM Disk Encryption

- **Encryption at host**:  
  - Option is **unchecked by default**.  
  - Enabling this enhances security by encrypting data before it reaches the VM's host.

2. OS Disk

- **OS Disk Size**:  
  - Default is based on the image selected (e.g., `127 GiB`).  
  - You can increase the size if your application requires more space.

- **OS Disk Type** *(choose from dropdown)*:
  - **Standard SSD (default)**: Balanced price and performance.
  - **Premium SSD** ⚡: For production workloads, offering low latency and high IOPS.
  - **Standard HDD** 💰: Most economical, best for dev/test workloads.

> Descriptions under the dropdown help you choose the right disk type for your use case.

3. Delete with VM

- **Checkbox**:  
  - When checked ✅, the OS disk is deleted when the VM is deleted.  
  - When unchecked ⬜, the OS disk is retained for reuse or backup.

4. Data Disks

- Add one or more **data disks** for additional storage.
- You can:
  - Create and attach new disks.
  - Attach existing disks.
- Configure:
  - **Disk Size**
  - **Disk Type** (SSD, HDD)
![Screenshot 2025-04-22 113553](https://github.com/user-attachments/assets/49593d80-24bf-4781-b54c-82eeca9c13a4)

---

After disk configuration is complete, click **"Next: Networking >"** to proceed to the next step.

## Step 5: Configure Networking

1. **Virtual Network**
- **Virtual Network (VNet)**:  
  Choose an existing virtual network or click **Create new** to define one.  
  VNets allow your VM to securely communicate with other Azure resources.

- **Subnet**:  
  Select a subnet within the VNet.  
  Subnets divide the VNet into smaller IP ranges and isolate resources.

2. **Public IP**
- **Public IP Address**:  
  Choose whether to assign a public IP to your VM.  
  - Selecting **None** means the VM won't be reachable from the internet.
  - You can also click **Create new** to generate a fresh public IP.

3. **NIC Network Security Group (NSG)**
- **NIC Network Security Group**:  
  Defines which inbound and outbound traffic is allowed to/from the VM's network interface card (NIC).

  - **Basic**: Select inbound ports like SSH (22) or RDP (3389).
  - **Advanced**: Attach an existing NSG with custom rules for better control.
![Screenshot 2025-04-22 113612](https://github.com/user-attachments/assets/284c0c39-37fb-4954-b3ad-ebfd07433060)

4. **Accelerated Networking**
- Toggle this ON or OFF based on the VM size and supported region.  
  Accelerated Networking improves performance by reducing latency, jitter, and CPU usage.

> This option is only available for supported VM sizes and OS images.

5. **Load Balancing**
- **Place VM behind a load balancing solution** (Optional):  
  Use this if you want to distribute traffic across multiple VMs.
  - Options include:
    - No load balancing
    - Azure Load Balancer
    - Azure Application Gateway
![Screenshot 2025-04-22 113621](https://github.com/user-attachments/assets/41b6d599-aea4-476d-a577-4c6f9c7ee30b)

---
Once all networking options are configured, click **"Next: Management >"** to proceed to VM monitoring and management settings.

## Step 6: Configure Management

The "Management" tab provides various options for managing your virtual machine after it's deployed. For this step, we can keep the default settings as well. 

1. **Microsoft Defender for Cloud**

- Azure provides free security management through the  
  **Foundational Cloud Security Posture Management Free Plan**.
- Helps detect threats and improve your VM’s security.

2. **Identity**

- **Enable System Assigned Managed Identity**:  
  - Toggle **On** to assign an identity to the VM so it can securely access Azure resources without credentials.

3. **Microsoft Entra ID (RBAC Login)**

- **Login with Microsoft Entra ID**:  
  - Allows login to the VM using Entra ID instead of local admin credentials.  
  - Requires **role assignment** (e.g., Virtual Machine Administrator Login or User Login).
![Screenshot 2025-04-22 113632](https://github.com/user-attachments/assets/8db3b5f1-bc11-4d34-b53a-3c82df8187b9)

---

Once these are set, click **“Next: Monitoring >”** to continue.

## Step 6: Configure VM Monitoring

Choose how you want to monitor your virtual machine's health and performance.

**1. Alerts:**

* **Enable recommended alert rules:** (Recommended) Get basic alerts for common issues automatically.

**2. Diagnostics:**

* **Boot diagnostics:** Helps troubleshoot startup failures.
    * **Enable with managed storage account:** (Recommended) Easiest way to enable boot logging and screenshots.
    * **Enable with custom storage account:** Use your own storage account.
    * **Disable:** Not recommended for troubleshooting.
* **Enable OS guest diagnostics:** (Optional) Collect performance metrics from inside the VM (CPU, memory, etc.).

**3. Health:**

* **Enable application health monitoring:** (Optional, Advanced) Monitor the health of specific applications within the VM.

**Recommendation:** For most users, **enabling recommended alert rules** and **boot diagnostics with a managed storage account** are good starting points. Consider enabling OS guest diagnostics for performance monitoring.
![Screenshot 2025-04-22 113655](https://github.com/user-attachments/assets/b53d5fb9-01bc-4134-ad4c-dbe833525b7d)

Click **"Next: Advanced >"** to continue.

## Step 7: Configure Advanced Settings (Keeping Defaults)

The "Advanced" tab provides additional, less commonly used configuration options for your virtual machine. These options typically include settings related to:

1. **Extensions:** Azure VM extensions are small applications that provide post-deployment configuration and automation tasks on Azure VMs.
2. **Custom data:** You can provide custom data, such as a cloud-init configuration, to customize your VM on first boot.
3. **Agent:** This relates to the VM agent that enables communication and interaction with the Azure fabric.
![Screenshot 2025-04-22 113707](https://github.com/user-attachments/assets/fad442a9-1850-4c98-b36d-f3a8b528170d)

For this walkthrough, we will keep all the default settings on the "Advanced" tab. This means you do not need to make any changes.
Move on tags

## Step 8: Add Tags (Optional)

The "Tags" tab allows you to assign metadata to your Azure virtual machine in the form of name/value pairs. Tags are helpful for organizing your resources, managing billing, and applying policies across multiple resources.

1. **Enter Name and Value:** In the provided fields, you can enter a name for your tag (e.g., "env") and its corresponding value (e.g., "dev").

2. **Associate with Resources:** The "Resource" column allows you to associate this tag with specific resources within the deployment. The screenshot shows "13 selected," indicating that this tag will be applied to the resources being created as part of this VM deployment.

3. **Add More Tags (Optional):** You can add multiple tags by clicking the "+" icon.

Adding tags is optional but highly recommended for better resource management and cost tracking in Azure, especially as your environment grows.

![Screenshot 2025-04-22 113716](https://github.com/user-attachments/assets/4d452819-6495-4dc0-9e46-7f4a2ed0a1b4)

**Proceed to Review and Create:** Once you have added the desired tags (or decided to skip this step), click the **"Next: Review + create >"** button to proceed to the final step of reviewing your configuration and creating the virtual machine.

## Step 9: Review and Create

The "Review + create" tab allows you to review all the settings you have configured for your virtual machine before deployment.

1.**Validation Passed:** At the top of the tab, you should see a "Validation passed" message with a green checkmark. This indicates that Azure has checked your configuration and found no critical issues that would prevent the VM from being created. If validation fails, you will see an error message, and you will need to go back to the relevant tabs to correct the issues.

2. **Price:** This section provides an estimated cost for running the virtual machine based on the size and region you selected. Review this information to ensure it aligns with your budget. It may show an hourly rate and indicate if any subscription credits are being applied.

3. **Terms:** This section displays the terms of use and privacy policy associated with the Marketplace offering you selected for the virtual machine image. Ensure you read and agree to these terms before proceeding.

4. **Review Your Configuration:** Take a moment to scroll through the summary of your configuration presented on this page. Double-check the selected virtual machine size, image, networking settings, disk configuration, and any other options you have chosen to ensure they are correct.

5. **Create the Virtual Machine:** Once you have reviewed your configuration and confirmed that everything is as desired, click the **"Create"** button to initiate the deployment process of your virtual machine in Azure.

6. **After Clicking "Create":**

* Azure will begin provisioning the resources for your virtual machine. This process may take a few minutes.
* You can monitor the deployment progress through notifications in the Azure portal.
* Once the deployment is complete, you will be able to access and manage your new virtual machine.
![Screenshot 2025-04-22 113724](https://github.com/user-attachments/assets/88f00bbe-b7e9-4b35-be81-23e742a4480f)
**Congratulations! You have successfully configured and deployed a virtual machine in Azure.**

  ## Step 10: Deployment Successful

Once you click "Create" on the "Review + create" tab, Azure will begin deploying your virtual machine. This process can take several minutes.

1. You can track the progress of the deployment through notifications in the Azure portal.

2. When the deployment is finished suessfully, you will see a page with the message "**Your deployment is complete**" displayed at the top, accompanied by a green checkmark.

3. This section provides information about the deployed resources.
![Screenshot 2025-04-22 113738](https://github.com/user-attachments/assets/042d5208-fe5e-4491-ae52-dc429b3db897)
4. To start using and managing your newly deployed virtual machine, click the **"Go to resource"** button. This will take you to the overview page for your virtual machine.

## Step 11: Connect to Your Virtual Machine

After clicking "Go to resource," you will be directed to the overview page of your virtual machine, where you can manage and interact with it. To connect to your virtual machine:

1. **Locate the "Connect" button.** This button is typically found at the top of the overview page. Click on the dropdown arrow next to it.

2. **Select your preferred connection method.** The dropdown menu will present different ways to connect to your VM. Options might include:

* **Connect** (likely using RDP for a Windows VM): This will typically download an RDP file for use with your local Remote Desktop Connection application.
* **Connect via Bastion:** A more secure, browser-based connection method that avoids exposing RDP directly to the internet.
![Screenshot 2025-04-22 113753](https://github.com/user-attachments/assets/c7ad9340-1326-43f1-ae68-13e102ec8d6d)
Choose the method that suits your needs and the configuration of your virtual machine. Follow the on-screen instructions for your chosen connection method.

## Step 12: Connect using Native RDP

After selecting "Connect," you will be presented with connection options. To connect using Native RDP (Remote Desktop Protocol):

1. **Verify Public IP Address:** The "Connecting using" section displays the public IP address of your virtual machine (e.g., 13.91.102.147). Take note of this IP address.

2. **Review Connection Details:** The page also shows the default RDP port (3389) and the administrator username you configured earlier (e.g., azureadmin).

3. **Download RDP File:** Click the **"Download RDP file"** button. This will download a `.rdp` file to your local computer. This file contains the necessary connection settings.
4. 
![Screenshot 2025-04-22 113800](https://github.com/user-attachments/assets/33aad754-c84a-4755-a202-134586cd94ab)

5. **Open the RDP File:** Once the download is complete, open the `.rdp` file. This will launch the Remote Desktop Connection application on your local machine.
6. 
![Screenshot 2025-04-22 113813](https://github.com/user-attachments/assets/3c6e50d3-7991-4f2a-96d3-4fd3b0cb8d94)

## Step 13: Connect via Remote Desktop Connection

**1. Connect to the Remote Computer:** You may see a warning about connecting to a remote computer. Click **"Connect"** to proceed.

![Screenshot 2025-04-22 113820](https://github.com/user-attachments/assets/cb04c06b-4de7-457e-86ec-b62a61940f91)

**2. Enter Credentials:** You will be prompted to enter your credentials. Provide the **username** (e.g., azureadmin) and the **password** you created when setting up the virtual machine.

![Screenshot 2025-04-22 113829](https://github.com/user-attachments/assets/026ba554-79e0-497f-8f0c-1dc9e1275b9c)

**3. Security Certificate:** You might receive a warning about the security certificate of the remote computer. You can usually click **"Yes"** or **"Don't ask me again for connections to this computer"** and then **"Connect"** to proceed.
![Screenshot 2025-04-22 113915](https://github.com/user-attachments/assets/68d1e5d5-dab7-4640-a565-798da5ee3019)

You should now be successfully connected to the desktop of your Azure virtual machine, and you can begin working with it.
