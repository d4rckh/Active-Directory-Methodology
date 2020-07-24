# Rough Process

- Setup responder and listen without poisoning.

- Watch the traffic flows.

- Locate the Domain Controller.

- Setup ntlmrelayx for a target that is valuable.

- Once a shell is obtained, start AD enum.

- Invoke-SharpHound in memory from the remote attacking host. (avoiding disk until absolutely necessary, can also send BloodHound files to remote source)

- PowerView in memory from the remote attacking host. (avoiding disk until absolutely necessary)

- PowerView Invoke-Kerberoast

- PowerView Invoke-ASREPRoast (Users with Pre-auth not required)

- Start cracking hashes from Kerberoast and ASREPRoast. (See password cracking materials)

- Import data into BloodHound.
  
  1. Look for "Reachable High Value Targets"
  2. Look for Domain Admins and sessions
  3. Look for local admin count on any compromised users.
  
**Back to [main page](README.md)**
