Sample input - chris alan<br>
output - Chris Alan<br>
<br>
input - hello    world  lol<br>
output - Hello    World  Lol<br>

```python
def solve(s):
    ram = s[0].upper()
    for i in range(1,len(s)):
        if(s[i-1] == " "):
            ram = ram + s[i].upper()
        else:
            ram = ram + s[i]

    return(ram)
```
