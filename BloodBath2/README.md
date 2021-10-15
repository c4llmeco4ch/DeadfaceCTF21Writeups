# Blood Bath 2

## Category

Forensics

## Point Value

15 Points

## Prompt

We've obtained access to a system maintained by bl0ody_mary. We believe bl0ody_mary stole a sensitive document and is storing it on her Linux machine. Search her system for any files relating to De Monne Financial.

Username: bl0ody_mary Password: d34df4c3

bloodbash.deadface.io:22

## Solution

Similar to Blood Bash, we can SSH in to the target machine and are greeted with the same directories.

A quick `ls` of the home directory provides us with a few places to check:

- Downloads
- Pictures
- Documents
- Music
- Videos

From Blood Bath, we checked Documents and only saw 1 file existed. But is that really true? If it's a sensitive document, maybe it's a hidden file? To check, we can run `ls -a Documents`. This shows us the existense of a second file: `.demonne_info.txt`. Running a `cat` command on the file provides us with the flag: flag{a856b162978fe563537c6890cb184c48fc2a018a}
