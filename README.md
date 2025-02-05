<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Deployed in Windows Server 2022 Virtual Machine </h1>
This tutorial outlines the implementation of on-premises Active Directory within Windows Server 2022 using VirtualBox<br />

<h2>Environments and Technologies Used</h2>

- VirtualBox
- Active Directory Domain Services
- Group Policy Management 

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 Pro

<h2>Deployment and Configuration Steps Covered in This Section</h2>

- Windows Server 2022 Setup

<h2>Deployment and Configuration Steps</h2>

Download VirtualBox & Windows Server 2022 ISO. An ISO file is a disk image file that contains the installation files for Windows Server 2022. 

Create a VM called “Domain Controller” with ISO attached, other Windows 64-bit, 8 GB of RAM, 1 CPU, and 50GB for the virtual hard disk size

Change the shared clipboard and drag-drop setting for the DC VM to bidirectional. 

![image](https://github.com/user-attachments/assets/2442ae6d-e777-4ac8-9fc8-ad5fbcf700d5)


In our DC VM, we need two NICs: one for internet connectivity (adapter 1) and one for the internal VirtualBox network (adapter 2). 

![image](https://github.com/user-attachments/assets/96141994-621c-4268-aad1-d2322eec4701)

Next, you can just run the DC VM and create your login credentials, then you can go ahead and proceed until the setup is complete. 

Go to settings and rename this pc to “DC”

To make the VM run faster, go to devices, insert guest additions cd image, then go to file explorer, VirtualBox Guest Additions, install the following application, and reboot. 

![image](https://github.com/user-attachments/assets/d644d104-c119-4bf3-857d-9969e63ee234)

Next, we will manually set up the internal NIC, go to network settings, and rename both networks for clarity. 

![image](https://github.com/user-attachments/assets/8e835a82-3235-4415-877e-090f3397225c)

Then go to internal adapter, properties, IPV4 

![image](https://github.com/user-attachments/assets/f0ade9b7-5b0f-48a5-8f43-05509ea5eb37)

Then assign a static IP address, subnet mask, and DNS server address for this internal adapter. 

![image](https://github.com/user-attachments/assets/fec17493-e361-453d-81e2-44a4bc7d21bb)


