# These Have Zealot's Prints All Over Them

## Category

Reverse Engineering

## Point Value

10 Points

## Prompt

A "hash" is a "digital fingerprint" of a file that is astronomically improbable to duplicate with other content by accident, and nearly impossible to duplicate intentionally. Therefore, it is often used as a "shorthand" to identify a file.

Calculate the SHA256 sum of TheZeal0t's cryptoware program, and its decryptor program. Enter the two hashes as the flag, separated by a pipe symbol, with the cryptoware's hash first, followed by the decryptor program's hash. Example:

flag{435524cc4113668d3f1e1e761d1717ba1bcf8b86b6dfaab9d048338e4e00a764|5d213aa47efd7e255c8304f56f148f87488a4bd9488f631ac4ed87f02c85cdce}

## Solution

This one depends a bit on your operating system, but Linux has `sha256sum` as a command. This causes the problem to be fairly trivial: run `sha256sum {encryptProgram}` then `sha256sum {decryptProgram}`. Combine those two with a pipe symbol ('|') in the middle and you get `flag{5a54fb61f7b1a9b1b7405602388add7e3323890bc74952a62803ffb1a535338b|969102c7feb6003624c4caf0e00fa9a60d96bc503ef0beb71ed4af68ba1fc047}`
