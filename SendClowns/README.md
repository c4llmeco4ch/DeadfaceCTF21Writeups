# Send in the Clowns

## Category

Stenography

## Point Value

10 Points

## Prompt

There is a secret hidden somewhere in this image. Can you find it? Submit the flag as flag{this-is-the-flag}. [](clowns.jpg)

## Solution

A good rule of thumb I like to test first when working with stenography problems is running a simple `strings` command on the file. Given we know the flag has a specific format, we can have the computer do most of our work for us with a simple command: `strings {file_name} | grep flag`. Running this produces one line: `flag{s3nd_in_the_kl0wns}`
