
- echo $string > $filename : overwrites file content and replaces it with whatever is echo
	- >> : two of these makes it append to the end of the file
# Process Management

- ps: report a snapshot of current procs 
	- ef: standard syntax -> just pid and other stuff
	- aux BSD format -> shows data like cpu and mem usage along with pid
-  renice: set priority of a process for cpu
	- -n : prio # (-19 - 20) -19 being highest prio
	- -m : PID 
- kill : kill process
	- -STOP : stops proc
	- -CONT : continues
	- -9 : force kills
	- -3 : kills threads
# User Commands

For a list of more specific commands check: 
https://github.com/iam-veeramalla/ultimate-linux-guide/tree/main/03-user-management
## User
*  useradd $username: add a user to /etc/passwd (with no password)
- adduser $username: ^ same as above but prompts for more info i.e. password , name, etc.
	- adds a home directory for that user
-  passwd $username: prompts you to make a password for that user
-  userdel $usrname: deletes user
- su - $username: signs into account
	- sudo su - : signs into root
- whoami: tells you who you're logged into
- logout
## Groups
- groupadd $groupname: make group
- usermod -aG $groupname $username : adds user to group

# File Commands

- chmod : change permissions of a file
- chown : change ownership of a file


# Misc

- nl : # of lines
- wc: word count
	- -m : # of chars
	- -l : # of \n