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
![ss-1](https://github.com/user-attachments/assets/17cdb76d-d567-4b29-9e0f-b0a07443e5cf)


**Create a Resource**
![ss-2](https://github.com/user-attachments/assets/927d5d06-f3a2-453e-bd7c-d5c3857a9c4b)

**Click on create**

### Step 3: Configure the VM Settings
1. **Basics**: Fill in the required fields such as Subscription, Resource Group, VM Name, Region, and Image.
2. **Size**: Choose the appropriate size for your VM based on your requirements.
3. **Administrator Account**: Set up the username and password for the VM.
4. **Inbound Ports**: Select the inbound ports you want to allow (e.g., SSH, RDP).

![ss-3](https://github.com/user-attachments/assets/347eb30d-af68-44d5-83ec-1471b6ce1547)
**Select a resource group and VM name**
![ss=4](https://github.com/user-attachments/assets/a639202b-89f6-4853-a070-1a46fa70049c)
**Select Image type and Machine Size**
![ss-5](https://github.com/user-attachments/assets/ab6dea83-4614-4645-bccb-95668756abb8)

**Add username and create a new SSH key also select inbound ports**
![ss-6](https://github.com/user-attachments/assets/e90420b7-9b6b-44ca-b572-06632ad4290c)

**Configure disk size and type**

### Step 4: Review and Create the VM
1. Review all the settings you have configured.
2. Click on **"Review + create"**.
3. After validation, click on **"Create"** to deploy the VM.
4. Download the SSH key and create resource.

![ss-7](https://github.com/user-attachments/assets/c9a1bf17-8fa2-4dfc-a447-a00e48f5940d)

**Click on Review and create**
![ss-8](https://github.com/user-attachments/assets/b6c0c54c-5783-4759-a73c-8f00e14ff883)

**Download the SSH key and create resource**
![ss-9](https://github.com/user-attachments/assets/d159dfc6-9768-44ec-90f7-669777bf85a4)

**Wait for deployment**
![ss-10](https://github.com/user-attachments/assets/88c503ab-bbc0-4ab4-8992-7576793d30e4)

**Deployment done**


### Step 5: Attach Storage to the VM
1. Once the VM is created, navigate to the **"Disks"** section under the VM settings.
2. Click on **"Add data disk"**.
3. Configure the new disk settings such as Name, Size, and Type.
4. Click on **"Save"** to attach the disk to the VM.
![ss-11](https://github.com/user-attachments/assets/f642e097-5d1f-46c1-b977-fcdacc612a62)
**In seetings tab, select **"Disks"**, click on **"Create and Attachne Disk"** and configure the disk settings**

### Step 6: Install and Run a Docker Container
1. **Install Docker**:
   - SSH into your VM.
   - Run the following commands to install Docker:
     ```sh
     sudo apt-get update
     sudo apt-get install -y docker.io
     ```
  ![ss-12](https://github.com/user-attachments/assets/31eaeb55-ca19-481d-86c6-a4f442db9e98)


2. **Start Docker Service**:
   - Start the Docker service and enable it to start on boot:
     ```sh
     sudo systemctl start docker
     sudo systemctl enable docker
     ```
![ss-13](https://github.com/user-attachments/assets/7536bdd4-f5fa-47de-831d-d81b768413f9)

 ![ss-14](https://github.com/user-attachments/assets/3064ca03-b0ec-498d-ad53-e4e80d6e968f)

  ![ss-15](https://github.com/user-attachments/assets/a2d753f8-209a-4065-92c9-f011f167a1cc)


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
