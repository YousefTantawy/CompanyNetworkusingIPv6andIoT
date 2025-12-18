# Company Network using IPv6 and IoT
## Description:
- This .pkt file contains a 10 department Company network each having IoT, IPv6 on each PC, and at least 10 users and 5 IoT devices
- The users obtain their IPv4 address using the DHCP server connected to the router network, and obtain IPv6 address using SLAAC technology from the routers
- To configure the DHCP:
	- Give the server a static ip address and connect it to the router
	- Go to services and select DHCP 
	- Write down your configurations
	- Since the router blocks all broadcast messages, we need to configure it as well
	- go to your router and choose the correct interface
	- type in the command "ip helper-address `DHCP server ip`"
- To configure the router for IPv6:
	- Go to router CLI and go to config
	- Run "ipv6 unicast-routing" which turns on the SLAAC technology
	- Go to desired interface and run the following:
		- ipv6 address "desired static address" 
		- no ipv6 nd managed-config-flag which tells the router to manage the ipv6 configuration
		- no ipv6 nd other-config-flag which tells the router to not look for services like DHCPv6
- To access IoT devices a Home Gateway is to be used in each department
## Features:
- Allows for safe data transmission thanks to firewall
- Organized structure and easy to add upon
- Each department can be in contact with each other without issue
- Strong backbone with 2 routers
- Access points in each department for stable internet
