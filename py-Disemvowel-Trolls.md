<h2>Introduction</h2>
Trolls are attacking your comment section!

A common way to deal with this situation is to remove all of the vowels from the trolls' comments, neutralizing the threat.

Your task is to write a function that takes a string and return a new string with all vowels removed.

For example, the string "This website is for losers LOL!" would become "Ths wbst s fr lsrs LL!".

Note: for this kata y isn't considered a vowel.

my solution:

```py

def disemvowel(string):
    return "".join(w for w in string if w.lower() not in "aeiou")
    
```

another solutions:


```py 

def disemvowel(s):
    return s.translate(None, "aeiouAEIOU")
    
def disemvowel(s):
    for i in "aeiouAEIOU":
        s = s.replace(i,'')
    return s
    
import re
def disemvowel(string):
    return re.sub('[aeiou]', '', string, flags = re.IGNORECASE)  
      
def disemvowel(string):
    return string.translate(None, 'aeiouAEIOU')
    
 ```
    
 
