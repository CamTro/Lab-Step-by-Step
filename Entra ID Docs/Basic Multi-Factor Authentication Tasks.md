# Step 1: Enable / Disable Per-user MFA settings

- Open Microsoft Entra admin centre at [https://entra.microsoft.com](https://entra.microsoft.com).
- Log in using credentials for your tenant.
- From menu on left, open Identity submenu
- Select Users and n select All users.
- Look at menu on top of new screen and find Per-user MFA.
- Select Per-user MFA.
- Put a mark in box next to Bhogeswar Kalita.
- Select Enable MFA from top of list.
- Read message box that pops up.
	- Note - This is a manual URL that you can email to user, if you want to let them know to set up MFA.
- Select Enable button.
	- Note that after a few seconds enforced shows up next to Bhogeswar’s name.

# Step 2: Review Service settings for MFA

- Open Microsoft Entra admin centre at [https://entra.microsoft.com](https://entra.microsoft.com).
- Log in using credentials for your tenant.
- From menu on left, open Identity submenu.
- Select Users and then select All users.
- Select Per-user MFA item.
- Select Service settings.
- Review settings you can configure:
	- Setting What is it for
	- App passwords re are some legacy apps that won’t work with MFA, use this setting to allow a user to keep using m.
	- Trusted IPs If your company has a specific set of IP-address ranges that are always known safe, you can allow users to by-pass MFA logging in.
	- Verification options Select methods you are willing to allow users to use for in second factor of authentication.
- Remember multifactor authentication on trusted device If your users are using a device that you trust, like a company managed laptop; you can allow retention of MFA approved status for a specified number of days.
- Select Discard button if you made any changes.
- This is one method of configuring MFA for your users.

# Step 3: View MFA account lockout settings

- Open Microsoft Entra admin centre at [https://entra.microsoft.com](https://entra.microsoft.com).
- Log in using credentials for your tenant.
- From menu on left, open Protection submenu.
- Scroll to bottom of list and select Show more.
- Select Multifactor authentication from menu.
- Select Account lockout from menu.
- Set following lockout values:
	- Field Value
	- Number of MFA denials to trigger account lockout 3
	- Minutes until account lockout counter is reset 180
	- Minutes until account is automatically unblocked 15
- Select Save option at top of your screen.
- Review some of or configuration options you have on MFA like:
	- Fraud alert
	- Block / unblock users
	- Notifications