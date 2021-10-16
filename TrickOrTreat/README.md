# Trick or Treat

## Category

Programming

## Point Value

200 Points

## Prompt

A user on Ghost Town created a game that he claims no one can beat. Check out the game and find the flag hidden inside. Submit the flag as: `flag{flag-goes-here}`.

## Solution

### Step 1

Unzipping the linked file (this step has already been done in this repository) provides us with some game assets and a Python script, `game.py`. Depending on how your terminal/IDE is positioned on the screen, you may not notice immediately that launching the game prints `flag{` directly to the console.

After some looking through the game file, however, you may notice the first two lines of the <b>MAIN</b> section (line 299) provide us a helpful clue for where to start our search:

```python
b = Msg()
print(b.prnt([31, 37, 26, 32, 64]))
```

Scrolling up to line 72 reveals the class in question: `class Msg:`. In it, we have our prnt function and a constructor. While we could investigate these two functions more closely (in particular, what `self.alpha` contains), the most important thing to consider is that the combination `31, 37, 26, 32, 64` seems to lead us towards our answer.

### Step 2

After acknowledging the importance of the sequence above, one migh be tempted to investigate certain hexadecimal strings riddled throughout the program. `abc` on line 6-7, `do_coll()` on lines 133-134, and perhaps most enticingly `self.hidden` on line 16 all appear as potential means to our flag-filled end. However, taking a step back and reviewing the code again proves that these strings are simply red herrings.

We already know `Msg.prnt([31, 37, 26, 32, 64])` puts us pretty close to our answer, so a better idea might be to see if that sequence or a similar pattern exists elsewhere in the code. Looking around reveals the existence of 2 critical functions: `set_pref()` on line 190 and `gs()` on line 194. In fact, `set_pref()` contains our previously found combination, while `gs()` directly calls upon `set_pref()` on line 196.

```python
def set_pref():
    return str(f'{b.prnt([31, 37, 26, 32, 64])}')


def gs():
    gs_ = [2, 26, 13, 19, 62, 28, 33, 54, 55, 45, 62, 29, 54, 55, 45, 33, 65]
    print(f"{set_pref()}{b.prnt(gs_)}")
```

Seeing as `set_pref()` almost assuredly prints `flag{` as seen during our initial running of the program, it's safe to assume `gs()` contains our flag. But how do we get that onto the console?

The simplest answer lies in altering where it all began--line 301. By changing `print(b.prnt([31, 37, 26, 32, 64]))` to `print(gs())`, running the program gives us just what we were hoping for: `flag{CaNT_ch34t_d34th}`
