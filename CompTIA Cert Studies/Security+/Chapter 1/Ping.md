A basic command that is used to test connectivity for remote systems. It can also be used to verify a system can resolve valid hostnames to IP addresses, test the Network Interface Card (NIC), and assess organizational security

The ping command checks connectivity by sending Internet Control Message Protocol (ICMP) echo request packages. Remote systems reply with ICMP echo reply packages, and if you receive echo replies, you know that the remote system is operational.

`ping[IP Address]` - sends four ICMP echo requests on Windows. Linux sends out echo requests until "Ctrl + C" is used

`ping -t[IP Address]` - mimic Linux behavior on Windows

`ping -c[IP Address]` - mimic Windows behavior on Linux

### Using Ping to Check Name Resolution

The name resolution process resolves a hostname (such as google.com) to an IP address. There are several elements of a name resolution. Typically, a computer queries a Domain Name System (DNS) with the hostname, and DNS responds with an IP address.

You can ping the hostname of a remote system and verify the name resolution is working

ping gcpapremium.com
	![[Pasted image 20240514141446.png]]

First line shows the ping resolved the hostname to its IP address. The replies from teh server indicate that it is up & running
### Beware of [[Firewalls]]

Ping replies from system means that the system is operational and reachable, but if it fails, it does not mean that the system is not operational or unreachable. A "Reply Timed Out" error could appear even if the system is functional.

Many Denial-of-Service (DOS) attacks use ICMP to disrupt services on internet-based systems. A ping flood attack attempts to disrupt systems by sending ping requests repeatedly. Admins can configure [[firewalls]] to block ICMP traffic or block ICMP echo requests, which prevents the attacks from succeeding.
### Using Ping to Assess Organizational Security

If firewalls and pings have been configured to block ping traffic, a ping can be sent to test that they work properly.

### HPing

Similar to `ping` command, but it can send pings using TCP, UDP, and ICMP

### ipconfig and ifconfig

"ipconfig" (Internet Protocol configuration) - shows the Transmission Control Protocol / Internet Protocol (TCP/IP) configuration information for Windows system. 
This includes:
	- IP address
	- subnet mask
	- default gateway
	- MAC address
	- address of a Domain Name System (DNS) server
	- shows the config info for all network interfact cards (NICs)
Linux systems us "ifconfig"
Some common usage:
	- `ipconfig` - provides basic info about the NIC, such as IP address, etc.
	- `ipconfig /all` and "ifconfig -a" - shows a comprehensive listing of TCP/IP configuration info for each NIC. Includes the media access control (MAC) address, the address of assigned DNS servers, and the address of a Dynamic Host Configuration Protocol (DHCP) server if the system is a DHCP client.
	- `ipconfig /displaydns` - Each time a system queries DNS to resolve a hostname to an IP address, it stores the result in the DNS cache, and this command shows the contents of the DNS cache, and this command shows the contents of the DNS cache. Also shows any hostname to IP address mappings in the host's files.
	- `ipconfig /flushdns` - Erase the contents of the DNS cache. Use this when the cache has incorrect info, and you want to ensure that the system queries DNS for up-to-date info.

#### LINUX ONLY
These commands are specific to Linux:
	- `sudo` - provides admin rights
	- `ifconfig eth0` - shows the config of the first Ethernet interface (NIC) on a Linux system. Multiple NICs use eth1, eth2, and so on. `wlan0` to view info on the first wireless interface.
	- `ifconfig eth0 promisc` - enables promiscuous made on the first ethernet interface. Promiscuous mode allows a NIC to process all traffic it receives. Normally, a NIC is in non-promiscuous mode, it ignores all packages not addressed to it.
	- `ifconfig eth0 -promisc` - disables promiscuous mode
	- `ifconfig eth0 allmulti` - enables multicast mode on NIC. Allows NIC to process all multicast traffic
	- `ifconfig eth0 -allmulti` - disables multicast mode
`ifconfig` is deprecated on Linux machines. There is a push to use the commands instead:
	- `ip link show` - shows interfaces along with some details
	- `ip link set eth0 up` - enables a network interface
	- `ip -s link` -shows statistics on the network interface