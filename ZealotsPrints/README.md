# These Have Zealot's Prints All Over Them

## Category

Reverse Engineering

## Point Value

10 Points

## Prompt

TBA

## Solution

This one depends a bit on your operating system, but Linux has `sha256sum` as a command. This causes the problem to be fairly trivial: run `sha256sum {encryptProgram}` then `sha256sum {decryptProgram}`. Combine those two with a pipe symbol ('|') in the middle and you get `flag{5a54fb61f7b1a9b1b7405602388add7e3323890bc74952a62803ffb1a535338b|969102c7feb6003624c4caf0e00fa9a60d96bc503ef0beb71ed4af68ba1fc047}`
