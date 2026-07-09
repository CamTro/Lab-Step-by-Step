# Step 1: Create a Centralised `_Groups` OU
- Open ADUC
- Right click the domain root
- Select New -> Organisational Unit
- Name the OU `_Groups`
- Ensure **Protect container from accidental deletion** is checked
- Select OK
# Step 2: Create the Helpdesk Group
- Right click the `_Groups` OU
- Select New -> Group
- Group Name: Helpdesk
- Group scope: Global
- Group type: Security
- Select OK
# Step 3: Create Additional Groups
- Repeat process from Step 2 to make two global security groups:
	- Accounting
	- ITSupport
# Step 4: Verify Group Creation
- Confirm all groups exist inside the `_Groups` OU
- Open a group to verify scope and type
# Why Global Security Groups?
- Global Security Groups are commonly used to represent roles or departments, such as Helpdesk or Accounting
	- These groups typically contain user accounts and are later nested into resource specific groups
# Step 5: Add Users to Groups (GUI)
- Add Alice Johnson to Helpdesk
	- Open the Helpdesk group
	- Select the Members tab
	- Select Add
	- Add user `ajohnson`
	- Select OK
- Add `bmartinez` to Accounting
- Add `cwalker` to ITSupport

## Powershell Equivalent:
``` 
$groupsOU = "OU=_Groups,DC=lab,DC=local"

New-ADGroup -Name "Helpdesk" -GroupScope Global -GroupCategory Security -Path $groupsOU
New-ADGroup -Name "Accounting" -GroupScope Global -GroupCategory Security -Path $groupsOU
New-ADGroup -Name "ITSupport" -GroupScope Global -GroupCategory Security -Path $groupsOU

Add-ADGroupMember -Identity "Helpdesk" -Members ajohnson
Add-ADGroupMember -Identity "Accounting" -Members bmartinez
Add-ADGroupMember -Identity "ITSupport" -Members cwalker
```

# Step 6: Verify Group Membership
- Open each group and confirm correct membership
	- Group membership changes take effect immediately
# Important Notes:
- Users gain access through membership of groups
- Groups are normally centralised, not branch-based
- This structure supports clean scaling and delegation