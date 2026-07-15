I dealt with an issue when setting up a new-hire's device (Surface Pro 11 Tablet) where I was unable to login with under the ReFlow's domain. The reason for it was due to the device not being able to access ReFlow's network. In order to fix this issue I had to connect via VPN under the **FortiClient VPN**.

When setting up a VPN for a new/used device, you need to access the device through the local admin account (**.\skyadmin**)
- You can find the login credentials through **IT Glue** under the company's site (i.e. ReFlow)

If the device does not already have the FortiClient VPN, here are the direct download links:
- Mac: https://links.fortinet.com/forticlient/mac/vpnagent
- Windows: https://links.fortinet.com/forticlient/win/vpnagent
- Windows ARM: https://links.fortinet.com/forticlient/winarm/vpnagent

You can either copy the link and paste it in the device's browser via Remote Desktop or go through Agent Browser and in **File Management** you can drag and drop the FortiClient installer from your device onto the intended directory right-side window.

![[Pasted image 20260714142939.png]]

![[Pasted image 20260714142903.png]]

After logging in, you will need to pull up two login credentials from **IT Glue** again:
1. VPN IPSEC
	- This is pretty much the configs for the FortiClient VPN
	- Under username is the IP address & password is the Pre-Shared Key (PSK)
	- Under notes contains the additional configs for the specific site's **IPsec VPN Encryption Proposal (IKE Phase 1 & Phase 2)**
		- **IKE Phase 1**
			- AES-128 / SHA-1
			- AES-256 / SHA-256
			- Diffie-Hellman (DH) Group 5
		- **IPsec Phase 2**
			- AES-128 / SHA-1
			- AES-256 / SHA-1
			- DH Group 5
	- You will need to enter these in its respective fields on the FortiClient VPN settings in order to connect to the intended site's network
2. VPN admin login
	- Once you have configured the settings properly, it will prompt you for login credentials in order to activate the VPN
	- Enter the username and password as you see on IT Glue