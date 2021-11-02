# **Project 3 Mind Map**
## Brute Force!
### Tasking at Hand
- [ ] Beginner Task: Single User / Multi Passwords
- [ ] Intermediate Task: Single Password / Multi Users
	- [ ] Traditional Brute Force: "AAA", "AAB", "AAC"
- [ ] Expert Task: Add Time Limits / Login Attempts ( 5 Attempts per 60 Seconds )



### Initial Assumptions
	Need a Brute Force Component
	Need a Passowrd Spray Component
	Need a Time Component
	Python version of Hydra or Other Password Tools
	
### Basic Ideas
- Test Single User / Single Password
- Test Single User / Multiple Passwords
	- Optional: Limit?
	- Optional: True Bruteforce?
	- Optional: List of Passwords?
- Test Multiple Users / Single Password
- Test Multiple Users / Multiple Passwords
	- Optional: Limit?
	- Optional: True Bruteforce? (This would be more like a Hail Mary... Not Ideal.. Maybe dont Implement )
	- Optional: List of Users
	- Optional: List of Passowords
- Optional: Multiple Protocols? (Not an Original Tasking; SSH, FTP, SMB, HTTP, etc)
- Optional: Auto Mangle? (Not an Original Tasking)
- Optional: Automatic Shell Option? (Would need to Dig into how this could work; May need to break up code into different modules)
	
	
### Question to Assumptions
- [ ] How do I Interact with SSH using Python with built-ins? (Sockets?)
- [ ] When interacting with diff SSH, how do I account for ea ver., custom prompts, etc? ( Expect? -> Is Expect built-in)
- [ ] What do I make into an object? if at all? ( The connection to SSH itself? )
- [ ] How do I implement threading? Should I?


### Pseudo Coding - What will it look like?
``` py
# Imports
import argparse

# Initial Variables

# Instantiate Argparse
parser = argparse.ArgumentParser()
pgroup = parser.add_mutually_exclusive_group("What Mode?")

pgroup.add_arg("-bf") # Brute Force Mode
pgroup.add_arg("-ps") # Pass Spray Mode
parser.add_arg("-u")  # Username
parser.add_arg("-p")  # Password
parser.add_arg("-f")  # Path to File
parser.add_arg("-o")  # Output File
parser.add_arg("-v")  # Verbose

class SSHConnection:
	def __init__(self, ipaddr, username, password)
		...
	
	def test_connection_to_ssh(self):
		test_connection(self.ipaddr)
	
	def test_for_open_ssh_port(self):
		check_protocol(ipaddr, port)
		

def open_file(filename): # Needed to Open a File or Files
	with open(filename) as open_file:
		return open_file

def main():
	do_main_stuff
	return main_stuff


if __name__ == "__main__":
	try:
		main()
		exit
	except:
		exit

```