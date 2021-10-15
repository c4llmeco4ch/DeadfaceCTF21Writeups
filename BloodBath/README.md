# Blood Bath

## Category

Forensics

## Point Value

10 Points

## Prompt

We've obtained access to a system maintained by bl0ody_mary. There are five flag files that we need you to read and submit. Submit the contents of flag1.txt.

Username: bl0ody_mary
Password: d34df4c3

bloodbash.deadface.io:22

## Solution

Port 22 is an immediate tip off we need to use SSH here to connect to the system. Running the command `ssh -l bl0ody_mary -p 22 bloodbash.deadface.io` then entering the password gives us access to the home directory of the target system.

A quick `ls` of the home directory provides us with a few places to check:

- Downloads
- Pictures
- Documents
- Music
- Videos

Of these, Documents seems like the best place to start. `ls Documents` provides us with the only file in the directory: flag1.txt. `cat Documents/flag1.txt` gives us exactly what we need: `flag{cd134eb8fbd794d4065dcd7cfa7efa6f3ff111fe}`
