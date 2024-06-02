This command allows you to view stats for TCP/IP protocols on a system. Also gives the ability to view active TCP/IP network connections
Some common commands:
	- `netstat` - displays a listing of all open TCP connections 
	- `netstat -a` - display a listing of all TCP and User Datagram Protocol (UDP)
	- `netstat -r` - display a routing table
	- `netstat -e` - displays details on network statistics, including how many bytes the system sent and received
	- `netstat -s` - displays statistics of packets sent or received for specific protocols, such as IP, ICMP, TCP, and UDP
	- `netstat -n` - displays addresses and port numbers in numerical order. Useful if you're looking for information related to a specific IP address or a specific port
	- `netstat -p protocol` - show statistics on a specific protocol, such as TCP or UDP
	- `netstat -p tcp` - only shows TCP statistics

A multitude of switches can be combined to sow different types of information. For example, show a list of ports that the system is listening on (`-a`), listed numerically (`-n`), for only TCP protocol (`-p tcp`), you could use this command:
	`netstat -anp tcp`

Netstat displays the state of a connection, such as `ESTABLISHED`, to indicate an active connection. Some common states:
	- `ESTABLISHED` - Normal state for the data transfer phase of a connection. Active open connection
	- `LISTEN` - Indicates the system is waiting for a connection request. The well known port a system is listening on indicates the protocol
	- `CLOSE_WAIT` - Indicates the system is waiting for a connection termination request
	- `TIME_WAIT` - The system is waiting for enough time to pass to be sure the remote system received a TCP-based acknowledgment of the connection
	- `SYN_SENT` - The system sent a TCP SYN (synchronize) packet as the first part of the SYN, SYN-ACK (synchronize acknowledgment), ACK (acknowledge)
	- `SYN_RECEIVED` - The system sent a TCP SYN-ACK packet after receiving a SYN packet as the first part of the SYN, SYN-ACK, ACK handshake process. It's waiting for the ACK response to establish the connection. An excessive number of SYN_RECEIVED states indicate a SYN attack where an attacker is flooding a system with SYN packets but never finalizes the connection with ACK packets

