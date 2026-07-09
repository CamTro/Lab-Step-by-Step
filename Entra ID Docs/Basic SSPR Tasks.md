# Step 1: View SSPR properties for a specific group

- Open  [Microsoft Entra admin centre](https://entra.microsoft.com) at https://entra.microsoft.com.
- Log in using credentials for your tenant.
- From menu on left, open Protection submenu and n select Password reset.
- Find Self service password enabled bar.
	- Value What it means.
	- None No users can use SSPR feature
	- Selected Only members of selected group(s) can use SSPR.
	- All All users can use SSPR feature
- Set value to Selected.
- Select text No groups selected.
- Mark Project23 group we created previously.
- Use Select button to complete your choice.
- Save your configuration.

# Sub-Step 1: View SSPR authentication methods

- Select Authentication methods from menu within Password reset.
- Select 1 as value for Number of methods required to reset.
	- Note - this value represents how many different ways user is required to sign-in to password reset tool, before y are allowed to reset their password. Note that using a password is not an option.
- Select Email, Mobile phone, and Mobile app code for Methods available to user.
	- Note - if you use Security Questions you have to specific number of questions user is required to create and answer.
- Use button at top to Save your choices.
- You have added an authentication method to your self-service password reset.

# Sub-Step 2: View SSPR registration

- Select Registration from menu within Password reset.
- Make sure Require users to register when signing in? value is set to Yes.
- Set Number of days before users are asked to re-confirm… to 90 days.
- Select Save to save your changes.

# Sub-Step 3: View SSPR reset notifications

- Select Notifications from menu withing Password reset.
- Leave Notify users on password reset? at default of Yes.
- Change Notify all admins when or admins reset their password? value to Yes.
- Use Save option to save your changes.