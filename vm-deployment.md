# Step-by-Step VM Deployment Manual

## Objective

The objective of this guide is to provide a clear, step-by-step approach to deploying Virtual Machines (VMs) efficiently and securely across various environments. It aims to equip IT professionals, system administrators, and DevOps engineers with the necessary knowledge and best practices to plan, configure, deploy, and manage VMs using automated and manual methods. This guide ensures consistency, scalability, and optimal performance in VM deployments, while aligning with organizational IT policies and cloud architecture standards.

## Task 1: Deployment of VM

In this Exercise, you will be deploying an VM 

1. On the **Azure portal**, click on search bar, search for **Vitutual machine** **(1)**, and select **Vitutual machine** **(2)**.

   ![image](https://github.com/user-attachments/assets/2f3a0acb-4753-454a-859f-6935e2bff15e)

2. In the **Compute infrastructure | Virtual machines** tab, click on **+ Create** **(1)** drop-down button and select **Azure Vitutual machine** **(2)**.

   ![image](https://github.com/user-attachments/assets/afcb66ae-8c8d-4d47-aeae-c9713cad9fef)

3. In the Basic tab fill the following details and click on **Next : Disk >** **(15)**

   - Subscription : Select **default Subscription** **(1)**.
   - Resource group: Select **Labvm RG** **(2)**.
   - Virtual machine name: enter the VM name as **lab-vm1** **(3)**.
   - Region : select **West US** **(4)**.
   - Availability Options : select **No infrastructure redundancy required** **(6)**.
   - Image : select **x64** **(7)**.
   - Size :  select **Standard-D2s-v3 - 2 vcpus, 8 GiB memory (₹7,105.66/month)** **(8)**.
   - Username  : provide username as **azureadmin** **(9)**.
   - Password :  create a **strong password** and confirm it **(10)**.
   - Public inbound ports : select **Allow selected ports** **(12)**.
   - Select inbound ports :  select **RDP (3389)** **(13)** from the drop down.
   - Licensing :  check both the  **boxes** **(14)**.
     
      ![image](https://github.com/user-attachments/assets/0ccfa84e-0ad7-460e-9504-eaa6f66dbfa9)
      ![image](https://github.com/user-attachments/assets/6c2411af-0c73-43f3-a1f0-fdce08b9d1cb)

4. In the Disks tab, select **Standard SSD (locally-redundant storage)** **(1)** as an OS Disk type and click on **Next : Networking >** **(2)**.

      ![image](https://github.com/user-attachments/assets/b06bb10b-7131-446d-8744-d5dfdfafd4cc)

5. Review the newly created **Virtual Network** **(1)** and **Subnet** **(2)** by default and click on **Review + Create** **(3)**.

      ![image](https://github.com/user-attachments/assets/91aeb79d-8315-4939-b65f-da324be04d29)

6. After the validation, click on **Create** **(1)**.

      ![image](https://github.com/user-attachments/assets/fa6bd1af-4d9f-47a9-92bb-7f217739fa2f)

7. You will be redirected to **CreateVm-MicrosoftWindowsServer.WindowsServer**, click on **Go to resource** **(1)**.

      ![image](https://github.com/user-attachments/assets/42e5ad8b-fd14-4bb6-a5a2-1c4945af8608)

8. Click on the drop down beside **Connect** **(1)** and again on **Connect** **(2)**

      ![image](https://github.com/user-attachments/assets/6e94f155-0d09-4298-b38b-b89e07ea7c86)

9. Click on **Download RDP file** **(1)**.

      ![image](https://github.com/user-attachments/assets/6cf06bb5-8b0e-4a0c-8a91-812e7dc42130)

10. Open the downloaded file and click on **Connect** **(1)** as shown below.

       ![image](https://github.com/user-attachments/assets/67def97d-3499-4a7e-81c4-7e9900ca2844)

11. Enter your **password** **(1)**.

       ![image](https://github.com/user-attachments/assets/4380c28a-9513-4990-9407-8789d3ecb984)

12. Finally click on **Yes** **(1)**.

      ![image](https://github.com/user-attachments/assets/716bbeb3-0271-4c7a-93ba-28100c0ce592)

   Congratulations, The virtual machine has been successfully created and initialized, and you have now transitioned into its environment. This means you are currently operating within the confines of, and under the control of, your newly provisioned virtual machine instance.
      ![image](https://github.com/user-attachments/assets/2f3be07a-7858-45e6-bb48-aca4c7af4c81)
