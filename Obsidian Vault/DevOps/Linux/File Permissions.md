For commands see [[Commands#File Commands]]

For more information go to:
https://github.com/iam-veeramalla/ultimate-linux-guide/tree/main/06-file-permissions
# Permissions

	1. r : read | for numbering it equals 4
	2. w : write | for numbering it equals to 2
	3. x : execute | for numbering it equals to 1
you
ls -ltr shows permissions of cwd

first col determines whether its file or dir with - (file) or d (dir)

next three are for user perms
middle three are for group perms
last three are for other perms

you cannot access a file (even if you have all the permissions for it) if you do not have the permissions for the folder.

# Defaults

umask defines default permissions for files and dirs

default is 755 for dir and 644 for files