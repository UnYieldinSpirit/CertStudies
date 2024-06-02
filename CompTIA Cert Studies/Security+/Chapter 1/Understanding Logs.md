Log entries help admins and security investigators determine what happened, when it happened, where it happened and who or what did it. When examining entries from multiple logs, personnel create an audit trail that identifies all the events preceding a security incident.

### Windows Logs

Windows logs can be viewed though Windows Event Viewer. Primary logs:
	- Security log - functions as a security log, on audit log, and an access log. It records auditable events such as successes and failures. Windows enables some auditing by default, but admins can add additional auditing
	- System - OS uses the system log to record events related to the functioning of the OS. Can include when it starts, shuts down, information on services starting and stopping, drivers loading or failing, or any other system component event deemed important by the system devs
	- Application log - records events sent to it by applications or programs running on the system. Any application has the capability of writing events in the Application log. Includes warnings, errors, and routine messages
If a system is attacked, you may be able to learn details of the attack by reviewing the OS logs. Depending on the attack, any of the OS logs may be useful

### Network Logs
Record traffic on the network. The logs are on a variety of devices such as routers, firewalls, web servers, and network intrusion detection/prevention systems. These typically can be manipulated to log specific info, such as logging all traffic that the device passes, all traffic that the device blocks, or both. Useful for troubleshooting connectivity issues and when identifying potential intrusions or attacks. Includes info like where the packet came from and where it's going. Includes IP addresses, MAC addresses, and ports.
Web servers typically log requests to the web server for pages. A typical entry includes the following data:
	- host - IP address or hostname of the client requesting the page
	- user-identifier - name of the user requesting the page (if known)
	- authuser - logon name of the user requested in the page, if the user logged on
	- date - date and time of request
	- request - actual request line sent by client
	- status - http status code returned to client
	- bytes - byte length of the reply

### Centralized Logging Methods
It can be difficult to routinely check all device logs on a network. A standard solution is to use a centralized system to collect log entries. Two popular methods are with a [[Security Information and Event Management Systems (SIEM)|SIEM]] system and with syslog protocol

### Linux Logs

Located in `/var/log/`directory. Can be viewed through System Log Viewer or by using the `cat` command from the terminal:

`cat /var/log/auth.log`

Some common Linux logs are listed below:
	- `var/log/syslog` - stores all system activity, including startup activity. Not the syslog protocol used to collect log entries from other systems.
	- `var/log/messages` - wide variety of general system messages. Includes some messages logged during startup, some messages related to mail, the kernel, and messages related to authentication
	- `var/log/boot.log` - includes entries when the system boots
	- `var/log/auth.log` - contains info related to successful and unsuccessful logins
	- `var/log/faillog` - info on failed login attempts
	- `var/log/kern.log` - info logged by system kernel, the central part of the Linux OS
	- `var/log/httpd/` - if the system is configured as an Apache web server, you can view access and error logs within this directory