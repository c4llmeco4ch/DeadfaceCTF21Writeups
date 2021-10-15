# Big Boss

## Category

Cryptography

## Point Value

10 Points

## Prompt

An anonymous tipster sent us this photo alleging that it's a note written by b3li3f1203. The tipster claims that the note was intended for someone who works at De Monne Financial. They also said it's likely that it has something to do with a phishing campaign. Provide the name of the target individual as the flag in this format: flag{FirstName_LastName}.

[The note in question](crypto04.png)

## Solution

The first thing that popped out at me was two words: `Xwaaws'g` and `rcb'h`. Considering there are only a few letters that commonly follow apostrophes, these letters seemed to be the best targets to begin solving the cypher. Considering the 'g' comes after what looks like a name, that is likely to be an 's'. Meanwhile, the 'h' comes after a 3 letter word, leading to that possibly being a "can't" or "don't". Thus, it's reasonable to assess 'h' might be a 't'.

Now, 'g' and 'h' are right after one another, as are 's' and 't'. With those in mind, a shift cipher comes to mind as a possible. By either creating your own script [or using a tool such as this](https://goto.pachanka.org/crypto/shift-cipher), we can deduce this a ROT14. If we note the section, `vwg pcgg`, that shifts back to `his boss`. Thus, shifting the name after comma, `Aofqig Pmbsf`, gives `Marcus Byner`.

Thus, using the format provided in the prompt, we arrive at the flag: `flag{Marcus_Byner}`.
