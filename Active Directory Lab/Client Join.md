# Step 1: Create Client VM in Azure
- Create new Azure VM
	- **Image:** Windows Server 2022 Datacenter
	- **Virtual Machine Name:** `CLIENT01`
	- **Size:** Small (B2s or similar)
	- **Resource Group:** Same resource group as the domain controller
	- **Virtual Network:** Same VNet as the domain controller
# Step 2: Connect to the Client VM
- Once deployment completes, connect via RDP
- Log in using the local administrator account

# Step 3: Configure DNS (Critical Step)
- Open **Network Connections**
- Right-click the active network adapter → **Properties**
- Select **Internet Protocol Version 4 (IPv4)**
- Select **Properties**
- Set **Preferred DNS server** to the domain controller’s private IP address
- Select **OK**

This is important because AD relies solely on DNS to locate domain controllers. An incorrect DNS is the most common cause for failing to join a domain

# Step 4: Join the Domain
- Open **Settings → System → About**
- Select **Join a domain**
- Enter your domain name (e.g., `lab.local`)
- Authenticate with a domain administrator account
- Restart the computer when prompted

# Step 5: What Happens During a Domain Join?
- A computer account is created in Active Directory
- A secure trust relationship is established with the domain
- The client begins authenticating against the domain controller
- Group Policy becomes applicable to the machine
- This behaviour is identical regardless of whether OS is Windows Server or Desktop

# Step 6: Verify Domain Join
- After reboot, log in with the domain administrator account you used to join the domain
- Confirm the device shows as domain-joined
- Locate the computer account in Active Directory
- By default, the computer appears in the **Computers** container

# Is this common in real environments?
- Normally, while end users typically run Windows Desktop, the underlying AD behaviour is the same. Many labs, test environments and jump hosts use Windows Server as a client