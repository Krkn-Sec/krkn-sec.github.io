## RedXen's Fun CrackMe
[Link](https://crackmes.one/crackme/622645fb33c5d46c8bcc019b)

---

### Solution
This CrackMe was quite simple as its difficulty rating predicted. All it does is take the username that you've typed and shift the alphabet by +4 to generate a password. I wrote a simple script that will generate the password for you based on the username you enter.

```Python
#RedXen's Fun CrackMe
#https://crackmes.one/crackme/622645fb33c5d46c8bcc019b
#Keygen solution by KrknSec

from string import ascii_lowercase as ALPHABET

def shift(message, offset):
	translate = str.maketrans(ALPHABET, ALPHABET[offset:] + ALPHABET[:offset])
	return message.lower().translate(translate)

print(shift(input("Input username and I'll give you the proper password: \n"), 4))

```

---

---

## A.Leon's Simple Password With Checksum
[Link](https://crackmes.one/crackme/621a478533c5d46c8bcc0004)

---

### Solution
This CrackMe was solved by identifying a string in the binary. The string in the binary was *xxxx4xx10*. This string represents the password format and the x's are wildcards with the "4" and "10" being required. With the password format being determined, I was able to create a script that will generate valid passwords.

```Python
#A.Leon's Simple Password With Checksum
#https://crackmes.one/crackme/621a478533c5d46c8bcc0004
#Keygen solution by KrknSec

import random
import string

def keyGen():
	i = 0
	
	while i < 10:
	
		randomSectionOne = random.choices(string.ascii_uppercase, k=4)
		randomSectionTwo = random.choices(string.ascii_lowercase, k=2)
		
		finalKey = ''.join(randomSectionOne) + "4" + ''.join(randomSectionTwo) + "10"
		print(finalKey)
		
		i = i + 1

keyGen()
```

---

