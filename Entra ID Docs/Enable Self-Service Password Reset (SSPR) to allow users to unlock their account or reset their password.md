
# Step 1: Enable SSPR:

- Sign in to Microsoft Entra admin centre as at least Authentication Policy Administrator
- Browse to Entra ID -> Password reset
- From Properties page, under option _Self-Service Password Reset enabled_ choose Selected
- If your group isn't visible, choose no groups selected then browse for and select your Microsoft Entra Group then choose Select
- Click Save to enable SSPR for select users

# Step 2: Select authentication methods and registration options

- From menu on left side of Authentication methods page, set Number of methods required to reset to 2.
- Choose Methods available to users that your organization wants to allow. For this tutorial, enable following methods:
	- Mobile app notification
	- Mobile app code
	- Email
	- Mobile phone
- To apply authentication methods, select Save.

# Step 3: Set up notifications and customisations

- From menu on left side of Notification page, set up following options:
- Set Notify users on password resets? option to Yes.
- Set Notify all admins when or admins reset their password? to Yes.
- To apply notification preferences, select Save.
- If Users need more help with SSPR process, contact your administrator link can be customised.
- From menu on left side of Customisation page, set Customise helpdesk link to Yes
- In Custom helpdesk email or URL field, provide an email address or web page URL that users can get more help from your organisation from
- To apply custom link, select Save

# Step 4: Test SSPR

- To see manual registration process, open a new browser window in InPrivate or incognito mode, and browse to [https://aka.ms/ssprsetup](https://aka.ms/ssprsetup). Microsoft Entra ID directs users to this registration portal when they sign in next time.
- Sign in with a non-administrator test user, like testuser, and register your authentication methods contact information.
- Once finished, select button marked Looks good and close browser window.
- Open a new browser window in InPrivate or incognito mode and browse to [https://aka.ms/sspr](https://aka.ms/sspr)
- Enter your non-administrator test users' account information, like testuser, characters from CAPTCHA, and n select Next.
- Follow verification steps to reset your password. When finished, you receive an email notification that your password was reset.