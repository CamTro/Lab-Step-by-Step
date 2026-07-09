
# Step 1: Create a new user

- Open Microsoft Entra admin centre
- Log in using credentials for your tenant.
- From menu on left, select User and n All users.
- Select + New user and n pick Create new user option.
- Enter requested information:
	- Field Value
	- User principal name BhogeswarK
	- Display name Bhogeswar Kalita
- Leave Mail nickname as is.
- Make a copy of Password (auto-generated) and store it in Notepad. You will need it later.
- Leave Accounted enabled checked.
- Select Properties tab:
- Set values for first and last name:
	- Field Value
	- First name Bhogeswar
	- Last name Kalita
	- Note that you can set User type to Member. If you pick Guest, it will restrict users capabilities.
- Scroll down to bottom of page.
- Set Usage location to United States or to whatever region you are in.
- Select Review + create button.
- Select Create.

# Sub-Step 1: Log in to confirm user

- Open an InPrivate browsing window.
- Connect to Microsoft Entra admin centre
- Enter username and password you just created.
	- Field Value
	- Username BhogeswarK@your tenant name.onmicrosoft.com
	- Password Auto generated password you saved
- If prompted follow on-screen instructions to complete MFA setup.
- Feel free to explore Microsoft Entra admin centre for a minute.
- Close InPrivate browsing window.

# Step 2: Add a license to user

- Open a new tab in your browser.
- Connect to Microsoft 365 admin centre at https//: admin.microsoft.com.
- If prompted, log in using credentials for your tenant.
- Find menu on left side of screen.
- Open Billing item in menu.
- Select Licenses from list.
- When list of licenses appears, select Microsoft Power Automate Free.
- Select + Assign licenses item.
- Choose BhogeswarK from list (user created in previous task).
- Select Assign button at bottom of page.
- Notice message that you have successfully assigned a license.
- Close tab with Microsoft 365 admin centre.

# Step 3: Invite an external user to your tenant

- If not already open - Open a browser and connect to Microsoft Entra admin centre
- If prompted, log in using credentials for your tenant.
- From menu on left, open Identity menu.
- Select Users then select All users.
- At top of page select + New User.
- Choose option to Invite external user from dropdown.
- Enter information for your new external user:
	- Field Value
	- Email [ExtUser@testemail.com](mailto:ExtUser@testemail.com)
	- Display name External User
	- Message Thank you for joining company for this short work project. We look forward to building this project together.
- Select Review + Create button.
- Select Create.

# Step 4: Assign a role to a user

- If not already open - Open a browser and connect to Microsoft Entra admin centre
- If prompted, log in using credentials for your tenant.
- In left menu find Identity section. Open it if not already opened.
- Select Users then select All users.
- Choose user Bhogeswar Kalita create in earlier task.
- From newly opened menu select Assigned roles.
- At top of screen select + Add assignment.
- From Select role dropdown menu choose role Attribute Definition Reader.
- Select Next button when it becomes available.
- Choose option Eligible for Assignment type.
- Select Assign.

# Sub-Step: Alternate method to assign a role to a user

- Look at Identity menu section on left side of screen.
- Select Show more option to see full Identity menu.
- From list of items in Identity menu, expand Roles & admins section.
- Select Roles & admins.
- Select Attribute Log Reader from list of roles.
- From top of screen select + Add assignment.
- From Select member(s) select No member selected text.
- From list of users choose Bhogeswar Kalita.
- Choose Select button at bottom.
- Select Next button.
- On Add assignments page choose Active for Assignment type.
- Note that you have to enter a justification for this role / user assignment.
- Enter justification User will be working as an Attribute log reader as their primary job. into box.
- Select Assign.

# Step 5: Bulk import users

- If not already open - Open a browser and connect to Microsoft Entra admin centre
- If prompted, log in using credentials for your tenant.
- From Identity menu, select Users and then select All users.
- From top of page, select Bulk operations drop-down arrow and n select Bulk create.
	- Note - Selecting Bulk create will open a new tile. This tile provides a Download link to a template file that you will edit to populate with your user information and upload to add bulk creation of users.
- Select Download to see a sample bulk user CSV file.
	- Note -  .csv template provides you with fields included with user profile. This includes required username, display name, and initial password. You can also complete optional fields, such as Department and Usage location, at this time. You do not need to fill out all fields.
	- Lab Tip - A sample CSV has been provided in  Allfiles/Lab1 folder – APL0501-BulkUser.csv.
- Open Notepad.
- Open SC300BulkUser.csv file.
- Search and replace existing value «>> with Your actual domain name.
- Save file.
- On Bulk create users dialog, select file folder icon on step 3.
- Path to Allfiles/Lab1 folder and select APL0501-BulkUser.csv file.
- Select Open.
	- Wait for notification that file uploaded successfully. Select Submit button to add users.
	- Note - After users have been created, you will be prompted that creation has succeeded.
- Close Bulk create users dialog.
- Check list of users to see your bulk created users.