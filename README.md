# Hybrid-Azure-Active-Directory-with-MFA


<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1></h1>



<h2>Video Demonstration</h2>



<h2>Environments and Technologies Used</h2>



<h2>Operating Systems Used </h2>



<h2>High-Level Deployment and Configuration Steps</h2>

1. Create an Azure Virtual Network (VNet)
2. Deploy a Windows Server VM and place it in the Vnet
3. Install Active Directory 
4. Create an Azure AD (Microsoft Entra ID) Tenant
5. Enable Azure AD (Microsoft Entra ID)  Connect on the On-Prem VM
6. Verify Sync Status
7. Enable Multi-Factor Authentication (MFA)
8. Set Conditional Access Policies
9. Test Authentication

<h2>Deployment and Configuration Steps</h2>

![Pasted image 20250228191832](https://github.com/user-attachments/assets/e52b2502-33b0-4e63-bf2c-f8391ec1f44f)


Navigate to Virtual Networks on Azure and click create as pictured above

![Pasted image 20250228195212](https://github.com/user-attachments/assets/ec630dc3-11d7-4af7-b260-2ca4f212ee12)

Click "Create new" and create a new resource group called "AD-Hybrid-lab" <br>
Name the Vnet "AD-Hybrid-VNET" <br>
then click "Review + create" and then click create again on the following screen to create the VNet
*Take note of your region in this case I'm keeping it East US we will reference this in the next steps*

![Pasted image 20250228195539](https://github.com/user-attachments/assets/8d6986e1-686c-4a5f-909c-57191158e23c)


Navigate to the Virtual machines page and click on create
![Pasted image 20250228201732](https://github.com/user-attachments/assets/5f52667a-ef25-4894-9047-0a6926c169e4)


Configure the following:
- In resource group: select the "AD-Hybrid-lab" group
- For the Virtual machine name: name it "Domain-Controller-1"
- Image: select "Windows Server 2022 Datacenter: Azure Edition - x64 Gen2"

*note: make sure this is in the same region as the vnet we created earlier in this case "East US" is in the same region*

