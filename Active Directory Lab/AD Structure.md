# Step 1: Open Active Directory Users and Computers (ADUC)
- Log into the domain controller
- Open Start Menu
- Search for and open **Active Directory Users and Computers**

# Step 2: Locate Domain Root
- In the left pane, expand your domain
	- This top level container is domain root

# Step 3: Create the `_Branches` OU
- Right click domain root
- Select **New -> Organisational Unit**
- Name OU `_Branches`
- Ensure **Protect container from accidental deletion** is checked
- Select **OK**

# Step 4: Create a Branch OU
- Right click `_Branches` OU
- Select **New -> Organisational Unit**
- Name OU after office Branch
- Ensure **Protect container from accidental deletion** is checked
- Select **OK**
# Step 5: Create Sub-OUs for the Branch
- Right click Branch OU
- Select **New -> Organisational Unit**
- Name OU Users
- Repeat to create `Workstations` and `Laptops`
- Ensure **Protect container from accidental deletion** is enabled on all OUs

# Step 6: Verify OU Structure
- Confirm OUs exist and are nested correctly
- Structure should look something like this (Example image):
![[Pasted image 20260709002000.png]]

In production environments, OUs are almost always organised around policy boundaries such as branch location


# Important Notes:
- Avoid placing users or groups in default containers
- Group Policy is applied at OU level, not containers