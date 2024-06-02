`chmod`
Short for change mode and is used to modify permissions on Linux system files and folders. Any file can read, write, and execute permissions.
	- Read (R) indicates someone can open the file and view its contents
	- Write (W) indicates a user can modify the contents. Generally combined with read
	- Executes (X) indicates a user can launch the file and is used with executable files
Additionally, permissions apply to three identities:
	- The first set of permissions applies to the owner of the files
	- The second set of permissions applies to the owner group
	- The third set of permissions applies to everyone else

It's common to use octal numbers (0-7) to set permissions. The following command gives read, write, and executable permissions to the owner, read and write to the owner group, and zero permissions to everyone else:
	`chmod 760 [filename]`

Quick table to display octal value meaning:

It's also possible to assign permissions using the text method. The following letters are used:
	`u` - file owner
	`g` - owner group
	`o` - all others

You can then assign permissions using `r`, `w`, and `x`. If you want to add read permission to the group, you would use this command:
	`chmod g=r [filename]`

You can remove permissions by using a dash, like so"
	`chmod o-x [filename]`
#linuxcommands