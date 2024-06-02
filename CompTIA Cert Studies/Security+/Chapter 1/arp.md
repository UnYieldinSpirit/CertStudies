`arp` command is used to view and manipulate the Address Resolution Protocol (ARP)

Some sample commands:
	- `arp` (Windows) - without a switch, shows help
	- `arp` (Linux) - without a switch, shows ARP cache
	- `arp -a` (Windows) - shows the ARP cache
	- `arp -a [IP address]` - displays ARP cache for specified IP address
`arp` can be used to identify the MAC address of other systems on your local network. Ping server1, and ARP will identify server1's IP address. `arp -a` to show ARP cache, which includes the MAC address for server1

