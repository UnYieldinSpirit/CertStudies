The syslog protocol specifies a general log entry format and the details on how to transport log entries. You can deploy a centralized syslog server to collect syslog entries from a variety of devices in the network, similar to how a SIEM server collects log entries. 

Any systems sending syslog messages are originators, while the entries are sent to collectors (a syslog server).

Syslog protocols only define how to format the syslog messages and send them to a collector

### syslog -ng and rsyslog

Two additional open source software utilities are used instead of syslogd on Linux-like systems. Based on syslog but provide additional extensions.
They are:
	- `syslog -ng` - Extends `syslogd`, allowng a system to collect logs from any source. Also includes correlation and routing abilities to route log entries to any log analysis tool. Provides rich filtering capabilities, content-based filtering, and can be extended with tools and modules written in other languages.
	- `rsyslog` - An improvement over `syslog -ng`. One significant change is the ability to send log entries directly into database engines.

### NXLog

Another log management tool similar to `rsyslog` and `syslog -ng`. Supports log formats from Windows, such as event log entries. Can be installed on both Windows and Linux-like systems. Functions as a log collector. and can integrate with most SIEM systems. It comes in two versions:
	- NXLog Community Edition - Propriety log management tool. Available for Windows and Linux. While free, it includes a feature set comparable with some SIEM solutions.
	- NXLog Enterprise Edition - Includes all Community features, but adds additional capabilities. Provides real-time event correlation and remote administration.