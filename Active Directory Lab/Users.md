# Step 1: Open Active Directory Users and Computers (ADUC)
- Log into the domain controller
- Open **Active Directory Users and Computers**
- Expand domain
- Navigate to `_Branches`, Office Name, `Users`

# Step 2: Create the First User (Alice Johnson in this)
- Right click the Users OU
- Select New -> User
- First Name: Alice
- Last name: Johnson
- User logon name: ajohnson
- Select Next

# Step 3: Set the User Password
- Set an initial password
- Uncheck **User must change password at next logon** (for lab specifically)
- Make sure **User cannot change password** is unchecked
- Ensure **Password never expires** is unchecked
- Select Next, then Finish

# Step 4: Create Additional Users
- Bob Martinez -> `bmartinez`
- Chris Walker -> `cwalker`

# Step 5: Verify User Creation
- Confirm all users appear in Users OU Branch
- Double click a user to view account properties
- Verify the Distinguished Name matches the correct OU path

# Important Notes
- In real environments, password behaviour is enforced by Group Policy and not manual user settings
- Users should always be placed in the correct branch OU
- Access is granted through group membership, not OU placement
- Password and lockout policies are enforced with Group Policy
