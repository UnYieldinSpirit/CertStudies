`grep`
Short for globally search a regular expression and print is used to search for a specific string or pattern of text with in a file
Example:
	`sudo grep "authentication failure" /var/log/auth.log`
		This shows only entries in the text "authentication failure" (without quotes). It's possible to use the `cat` command and the `grep` command together:
			`sudo cat /var/log/auth.log|grep "authentication failure"`
				This reads the file with `cat` and then pipes the results to the `grep` command

The pipe operator (`|`) allows to send the results of the first command to the second command