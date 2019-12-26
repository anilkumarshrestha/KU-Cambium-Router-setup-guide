# KU-Cambium-e400-setup-guide


default ip: 192.168.0.1
default username and password: admin

1. Setting up the router


Configure->System

	Set Name: KUCC

	Set Country-Code: China or India (Closest to Nepal)

Configure->Network->VLAN

	Add new L3 Interface (VLAN) if not created already.

	VLAN 1 is the Default VLAN

	Static IP: 192.168.xx.xx ( Provided by ISMS.)

	Network Mask: 255.255.255.0

Configure->Network->DHCP

	Create DHCP Pool

	Set address range: 192.168.1.10 - 192.168.1.254 ( This can be of your choice)

	Default router IP: 192.168.1.1 ( You can use this to access the router)

	DNS Address: 101.251.6.5 (This is KU's DNS) and 1.1.1.1 (Domain name for client)

	Network: 192.168.1.0 and 255.255.255.0 (Subnet number and mask of DHCP address pool)

Configure->Network->VLAN
	
	Default Gateway: 192.168.25.1

	DNS Server 1: 101.251.6.5 (Again KU's DNS)

	DNS Server 2: 1.1.1.1

Configure->Network->VLAN

	Create VLAN 2

	Static IP: 192.168.1.1

	Network Mask: 255.255.255.0

	NAT: "checked"

	Default Gateway: 192.168.25.1

	DNS Server 1: 101.251.6.5 (Again KU's DNS)

	DNS Server 2: 1.1.1.1

Configure->Network->WLAN

	Add WLAN

	Mesh: Off

	SSIS: KUCC

	VLAN: 2 (The one we created earlier)

	Security: WAP2 Pre-shared Keys

	Passphrase: your password here

	Radio: 2.5GHz and 5GHz(You can create two different WLAN for 2.5GHz and 5GHz)

	
And that's it. You are ready to rock and roll.


2. Reset

		Press and hold "Reset button" for 10 seconds.

		Connect Router to PoE and then PoE(LAN) to Computer

		Go to Network and Sharing center->LAN Properties->Properties->Internet Protocol Version 4->Use the following address

		IP address: 192.168.xx.xx or 192.168.25.1 or 192.168.1.1

		Subnet Mask: 255.255.255.0

		Default gateway: 192.168.25.1

		DNS: 1.1.1.1



Now you should be able to access the router from browser and follow Setting up the router above.

	


	
	
