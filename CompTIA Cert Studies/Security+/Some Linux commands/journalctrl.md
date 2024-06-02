`journalctrl`
Queries the Linux system logging utility (`journald`) and displays log entries from several sources. Can't query `journald` directly because it stores log data in a binary format, but `journalctrl` displays the data as text

`journalctrl -- since "1 hour ago"` - displays logs only from the last hour

`journalctrl -- list-boots` - shows available boot logs
`journalctrl-1` - shows boot log identified with the number "-1"

Any command that sends output to the display, you can redirect the output to a text file using the redirect operator (`>`). The following command sends the output to the text file named "myjorurnal.txt"

`journalctrl -- since "1 hour ago" > myjournal.txt`