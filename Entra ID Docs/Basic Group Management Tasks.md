# Step 1: Create a Microsoft 365 group

- Open Microsoft Entra admin centre at [https://entra.microsoft.com](https://entra.microsoft.com).
- Log in using credentials for your tenant.
- From menu on left, select Groups and n All groups.
- Select New group option.
- Enter requested information:
	- Field Value
	- Group type Microsoft 365
	- Group name Project23
	- Group description This group consists of members of new AI Simulation software with codename Project23
	- Membership type Assigned
- Under Members heading, select No member selected.
- Add Bhogeswar Kalita, by marking box and choosing Select button.
- Select Create button.

# Step 2: Create a Security group

- Open Microsoft Entra admin centre at [https://entra.microsoft.com](https://entra.microsoft.com).
- Log in using credentials for your tenant.
- From menu on left, select Groups and n All groups.
- Select New group option.
- Enter requested information:
	- Field Value
	- Group type Security
	- Group name Guest Users
	- Group description This group has all Guest users currently in tenant.
	- Membership type Dynamic User
- Under Dynamic user members heading, select Add dynamic query.
- Create a dynamic query with following values:
	- Field Value
	- Property userType
	- Operator Equals
	- Value Guest
- Select Save item from top of page.
- Select Create button.
	- Note - It will take up to 2 minutes for group to be populate.
- From Groups select Refresh item.
- Select Guest Users group we just created.
- Select Members.

# Step 3: Add an existing user to a new group.

- Open Microsoft Entra admin centre at [https://entra.microsoft.com](https://entra.microsoft.com).
- Log in using credentials for your tenant.
- From menu on left, select Groups and n All groups.
- Select Project23 group we created in Task 1.
- Select Members option from menu.
- Select + Add members from menu near top.
- Mark box next to External User and use Select button.

# Sub-Step 1: - Alternative method to add an existing user to a new group.

- Open Users menu, n select All users.
- Find and select External User from list.
- Select Groups item from menu.
- Select option to + Add memberships.
- Mark an existing group and use Select button to add m.

# Step 4: Add licenses and owners to a group

- Open Microsoft Entra admin centre at [https://entra.microsoft.com](https://entra.microsoft.com).
- Log in using credentials for your tenant.
- From menu on left, select Groups and n All groups.
- Select Project23 group we created in Task 1.
- Choose Owners option from menu.
	- Note - Your tenant administrator will automatically be added as owner of a group, if no owner is specified.
- Select  + Add owners menu item.
- Mark box next to Bhogeswar and use Select button.
- Notice new owner has been added to group.

# Sub-Step 1: Adding a license to a group

- Open a new tab in your browser.
- Connect to Microsoft 365 admin centre at [https://admin.microsoft.com](https://admin.microsoft.com).
- From menu on left, open Billing section and select Licenses.
- Select Microsoft Power Automate Free license.
- Choose Groups tab from newly opened screen.
- Select + Assign licenses item.
- Use dropdown on right side of screen to select Project23 group created earlier.
- Use Assign button at bottom of screen.
- Close You assigned licenses… notification.
- Use Refresh button to see added group licenses.