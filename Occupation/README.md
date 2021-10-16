# Occupation

## Category

OSINT

## Point Value

20 Points

## Prompt

Which employee at De Monne Financial was the target of DEADFACE that resulted in a data leak? Submit the employee's job title as the flag: flag{Job Title}

## Solution

Funnily enough, I found the solution to this on accident. I was originally looking at "The Count" and reading [the thread](https://ghosttown.deadface.io/t/what-programming-needs-are-there/56/4) linked. Looking around, I clicked on spookyboi's account. Under "Top Links" was a post titled "They Got the Wrong Guy". It was here that I remembered this task existed. Clicking this led me to a thread regarding someone who had gotten arrested wrongfully. Reading the article, it mentions someone by the name of Jimmie Castora. Searching `Jimmie Castora De Monne` using DuckDuckGo led to a LinkedIn profile for Jimmie Castora, the Senior Directives Organizer. Using the flag format requested leads us to the correct flag: `flag{Senior Directives Organizer}`.
