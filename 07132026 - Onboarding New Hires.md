When onboarding new hires for our clients, there **IS** a specific order:
1. Add user on Active Directory
2. Adjust Active User's permissions and settings on O365 Admin Portal

Depending on the company, you want to adhere to their setup. For example, ReFlow has a Windows Server with Active Directory along with Microsoft Office 365.

Typically you would:
1. Go to the company's Windows Server
	- This can be found on Datto → Sites → All Sites → Server → then access the correct server through **Web Remote**
		![[Pasted image 20260713170043.png]]
2. On their Active Directory, you want to right click on the folder of Active Users, then click **New** → **User**
3. Add the new hire's first and last name
4. User logon name follows the format: {**first name initial**}{**last name**}@companydomain.com
	- Make sure that the domain does not end with "**.local**"
	- ex) John Henry would be jhenry@reflowmedical.com
5. After creating, double click on the new user in the list of users in AD
	- Under **General** tab:
		- Under **Description**, add their job title
	- Under **Organization** tab:
		- Add **Job Title**, **Department**, and **Company**
6. On the Windows Server desktop, you will find a file named **ADSYNC.ps1**
7. In order to run the file, right-click it and click **Run with Powershell**
	- When done, it will prompt you to click Enter; click Enter on your keyboard
8. Then go to the company's admin portal (ex: ReFlow's O365 admin portal)
9. Update whatever needed permissions for groups and add the correct license
	- Typically **Microsoft 365 Business Standard** will do unless specified