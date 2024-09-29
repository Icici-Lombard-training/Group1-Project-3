# Creating a VM Instance in Azure and Attaching Storage

## Introduction
This guide will walk you through the process of creating a Virtual Machine (VM) instance in Microsoft Azure and attaching additional storage to it.

## Prerequisites
Before you begin, ensure you have the following:
- An active Azure subscription
- Access to the Azure portal

## Step-by-Step Guide

### Step 1: Log in to the Azure Portal
1. Open your web browser and navigate to the [Azure portal](https://portal.azure.com).
2. Enter your credentials to log in.

### Step 2: Create a New VM Instance
1. In the Azure portal, click on **"Create a resource"**.
2. Select **"Virtual Machine"** from the list of available resources.
3. Click on **"Create"** to start the VM creation process.

![Create a Resource](/media/ss-1.PNG)
**Create a Resource**
![Click on create](/media/ss-2.PNG)
**Click on create**

### Step 3: Configure the VM Settings
1. **Basics**: Fill in the required fields such as Subscription, Resource Group, VM Name, Region, and Image.
2. **Size**: Choose the appropriate size for your VM based on your requirements.
3. **Administrator Account**: Set up the username and password for the VM.
4. **Inbound Ports**: Select the inbound ports you want to allow (e.g., SSH, RDP).

![Select resource groups and VM name](/media/ss-3.PNG)
**Select a resource group and VM name**
![Select Image type and Machine Size](/media/ss=4.PNG)
**Select Image type and Machine Size**
![Add username and create a new SSH key also select inbound ports](/media/ss-5.PNG)
**Add username and create a new SSH key also select inbound ports**
![Configure disk size and type](/media/ss-6.PNG)
**Configure disk size and type**

### Step 4: Review and Create the VM
1. Review all the settings you have configured.
2. Click on **"Review + create"**.
3. After validation, click on **"Create"** to deploy the VM.
4. Download the SSH key and create resource.

![Click on Review and create](/media/ss-7.PNG)
**Click on Review and create**
![Download the SSH key and create resource](/media/ss-8.PNG)
**Download the SSH key and create resource**
![Wait for deployment](/media/ss-9.PNG)
**Wait for deployment**
![Deployment done](/media/ss-10.PNG)
**Deployment done**


### Step 5: Attach Storage to the VM
1. Once the VM is created, navigate to the **"Disks"** section under the VM settings.
2. Click on **"Add data disk"**.
3. Configure the new disk settings such as Name, Size, and Type.
4. Click on **"Save"** to attach the disk to the VM.

![In seetings tab, select **"Disks"**, click on **"Create and Attachne Disk"** and configure the disk settings](/media/ss-11.PNG)
**In seetings tab, select **"Disks"**, click on **"Create and Attachne Disk"** and configure the disk settings**

### Step 6: Install and Run a Docker Container
1. **Install Docker**:
   - SSH into your VM.
   - Run the following commands to install Docker:
     ```sh
     sudo apt-get update
     sudo apt-get install -y docker.io
     ```
    ![Installing Docker](/media/ss-12.PNG)

2. **Start Docker Service**:
   - Start the Docker service and enable it to start on boot:
     ```sh
     sudo systemctl start docker
     sudo systemctl enable docker
     ```
     ![starting docker](/media/ss-13.PNG)
     ![](/media/ss-14.PNG)
     ![](/media/ss-15.PNG)

3. **Pull a Docker Image**:
   - Pull a Docker image from Docker Hub, for example, Nginx:
     ```sh
     sudo docker pull nginx
     ```
     
4. **Run a Docker Container**:
   - Run a Docker container using the pulled image:
     ```sh
     sudo docker run -d -p 80:80 nginx
     

## Conclusion
You have successfully created a VM instance in Azure and attached additional storage to it. You can now use this VM for your applications and workloads.

## Contributors
Siddhesh Khope	1042256
Swapnil Vishwakarma	1042493
Shivam Jha	1042492
Sugandha Kumari	1042282
