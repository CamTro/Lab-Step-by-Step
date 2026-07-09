# Step 1: Start the Promotion Wizard
- Open Server Manager
- Select Notification flag at top of window
- Click Promote this server to a domain controller

# Step 2: Deployment Configuration
- Select Add a new forest
- Root domain name: local.homelab (for Homelab)

# Step 3: Domain Controller Options
- **Forest Functional Level:** Leave default
- **Domain Functional Level:** Leave default
- **DNS Server:** Checked (default)
- **Global Catalogue (GC):** Checked (default)
- **Directory Services Restore Mode (DSRM) Password:** DSRMRecovery1!

# Step 4: DNS Options
- May see warning about DNS Delegation
	- Expected in lab environment
- Select **Next**

# Step 5: Additional Options
- **NetBIOS domain name:** Accept the default

# Step 6: Paths
- Leave database, log files and SYSVOL paths at their defaults