# 1: Configure Password Policy (Domain-Wide)
-     Open Group Policy Management
- Expand Forest → Domains → lab.local
- Right-click Default Domain Policy → Edit
- Navigate to:
	- Computer Configuration
	- Policies
	- Windows Settings
	- Security Settings
	- Account Policies
	- Password Policy
		- Configure Maximum password age
		- Configure Minimum password length
# 2: Create a Basic Logon Script
-     Create a new text file named logon.bat
- Add the following line:
	- `echo Welcome to the domain`
- Save the file to the domain’s SYSVOL share
	- The full path will look like:
		- C:\Windows\SYSVOL\sysvol\lab.local\scripts
- Open Active Directory Users and Computers
	- Open a user account
	- On the Profile tab, enter logon.bat in the Logon script field
# 3: Delegate Password Reset Permissions to Helpdesk:
- Right-click the branch **Users** OU (for example: `_Branches → Houston → Users`)
- Select **Delegate Control**
- Add the **Helpdesk** group
- Select the following tasks:
	- **Reset user passwords**
	- **Force password change at next logon**
# 4: Move the Client Computer into the Correct Branch OU

- Open Active Directory Users and Computers
- Locate the computer account (e.g., CLIENT01)
- Drag the computer into _Branches → Houston → Workstations