# Step 1: Log into Client as Domain User
- On the client VM login screen, select **Other user**
- Log in using a domain account (for example: `LAB\ajohnson`)
- Enter the password you set earlier
- Complete the login
# Step 2: Verify Login Success
- The desktop loads successfully
- No local account is used
- The session is authenticated against the domain
# Step 3: Verify User in Active Directory#
- On domain controller:
	- Open ADUC
	- Navigate to Users OU in Office Branch
	- Confirm user account exists and is enabled
# Step 4: Verify Group Membership from Client
- On Client VM, open Command Prompt and run `whoami /groups`
	- Review output and confirm user is member of expected security group
- This proves several things
	- User received valid Kerberos access token
	- Group membership was evaluated at logon
	- Authorisation decisions can now be made
- Command is commonly used by administrators when troubleshooting access and permission issues

# Common Issues and What They Mean
- -Login fails immediately → DNS or domain join issue
- Username or password is incorrect when using `ajohnson` → Windows may be trying a local account; use `LAB\ajohnson` or `ajohnson@lab.local`
- `LAB\ajohnson`is recognized but Remote Desktop says the sign-in method is not allowed → add the user or their AD security group to the client's local **Remote Desktop Users** group
- Login works but groups are missing → group membership or token issue
- User logs in locally → incorrect username format
- Group changes not reflected → user must log out and back in