SIEM systems provide a centralized solution for collecting, analyzing, and managing data from multiple sources. It combines the services of security event management (SEM) and security information management (SIM) solutions. 

SEM provides real-time monitoring, analysis, and notification of security events, such as suspected security incidents. 

SIM provides long-term storage of data, along with methods of analyzing the data, looking for trends, or creating reports needed to verify compliance with laws or regulation.

SIEM systems are very useful in large enterprises that have massive amounts of data and activity to monitor. These systems use scripts to automate monitoring and reporting.

Typical SIEMs have common capabilities, here are some shared by most SIEMs:
	- **Log collectors** - collects data from devices throughout the network and stores these logs in a searchable database
	- **Data inputs** - log entries come from various sources, such as firewalls, routers, network intrusion detection and prevention systems and more. They can also come from any system that an organization wants to monitor, such as web servers, proxy servers, and database servers
	- **Log aggregation** - collects data from multiple systems, and these systems typically format log entries differently. The SIEM system can aggregate the data and store it so that it is easy to analyze and search
	- **Correlation engine** - a software component used to collect and Analyze event log data from various systems within the network. It typically aggregates the data looking for common attributes. It then uses advanced analytic tools to detect patterns of potential security events
	- **Reports** - Built-in reports. Typically grouped in different categories such as network traffic event monitoring, device events, threat events, threat events, logon/logoff events, compliance with specific laws, and more. Security professionals can create their own reports by specifying filters.
	- **Packet capture** - Protocol analyzers (sometimes called sniffers) capture network traffic allowing admins to view and analyze individual packets.
	- **User behavior analysis (UBA)** - Focuses on what users are doing, such as what applications they are launching and their network activity. Some UBA processes watch critical files looking for who accessed them, what they did, and how frequently they access these files. UBA typically looks for abnormal patterns of activity that may indicate malicious intent. Some data loss prevention (DLP) systems include this ability.
	- **Sentiment analysis** - Generally, this refers to analyzing text to detect an opinion or emotion. Within a SIEM system, it refers to using UBA technologies to observer use behaviors to detect unwanted behavior. This is no small feat and typically relies on artificial intelligence to analyze large data sets
	- **Security monitoring** - A SIEM typically comes with predefined alerts, which can provide continuous monitoring of systems and provide notifications of suspicious events. For example, if it detects a port scan on a server, it might send an email to an admin group or display the alert on a heads-up display. SIEMS also include the ability to create new alerts.
	- **Automated triggers** - Triggers cause an action in response to a predefined number of repeated events. Example, a trigger for failed logons is set at five. If an attacker repeatedly tries to log on to a server using [[Secure Shell (SSH)]], the server's log will show the failed logon attempts. When the SIEM detects more than five failed SSH logons, it can change the environment and stop the attack.
	- **Time Synchronization** - All servers sending data to the SIEM should be synchronized with the same time. Multiple locations sending data to a centralized SIEM with different time zones would prove problematic, that is why all of the servers should be on the same time.
	- **Event Deduplication** - Process of removing duplicate entries. A [[Network Intrusion Detection System (NIDS)]] collects data from a firewall while a SIEM collects data from the NIDS and the firewall. SIEM stores a single copy of any duplicate entries but ensures the entries are associated with both devices.
	- **Logs/WORM** - A SIEM usually has ways to prevent anyone from modifying log entries. Sometimes referred to as write once read many (WORM). As logs are received, the SIEM aggregates and correlates the log entries. After processing the logs, it can archive the source logs with write protection. 

Location of the SIEM varies based on how the SIEM is used. It's common to locate the SIEM within the private network, even if it collects data from a screened subnet. The internal network provides the best protection for the log data.

A SIEM dashboard gives admins views of meaningful activity. They provide continuous monitoring and real-time reporting. In a large network operations center (NOC), the SIEM might display alerts on  a large heads-up display. Smaller network, a single computer may suffice.

Common elements of a SIEM dashboard are:
	- **Sensors** - Many SIEM systems use agents placed on systems throughout a network. These collects logs from devices and send those logs to the SIEM systems.
	- **Alerts** - After setting triggers in a SIEM systems, it sends out alerts when the event fires. These alerts may trigger specific responses, but they are also displayed in the dashboard.
	- **Sensitivity** - Setting sensitivity with triggers and alerts to limit false positives while avoiding false negative.
	- **Correlation** - As log entries arrive, the SIEM correlates and analyzes the data.
	- **Trends** - As the SIEM system is analyzing the data, it can identify trends. For example, if there is suddenly a high rate of failed logins, it can identify the trends and raise an alert.
