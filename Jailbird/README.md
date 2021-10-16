# Jailbird

## Category

- Bonus
- OSINT

## Point Value

20 Points

## Prompt

It looks like authorities arrested a member of DEADFACE. But who was it?

Submit the member's username as the flag: `flag{username}`

## Solution

First, we start off by [going to the thread in question](https://ghosttown.deadface.io/t/what-they-got-our-boy/80). At the bottom of the thread, "d34th" responds to "...are we sure that's actually a DEADFACE member?" with "Yep, @dr.acula"

We can verify this by returning to the [original misdirection thread](https://ghosttown.deadface.io/t/they-got-the-wrong-guy/75/6), where d34th establishes "Looks like @dr.acula is in the clear then". 

Formatting the flag correctly leaves us with: `flag{dr.acula}`
