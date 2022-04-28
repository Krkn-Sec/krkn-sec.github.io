## RedXen's Fun CrackMe
[Link](https://crackmes.one/crackme/622645fb33c5d46c8bcc019b)

---

### Solution
This CrackMe was quite simple like its difficulty rating predicted. All it does is take the username that you've typed and shift the alphabet by +4. I wrote a simple script that will generate the password for you based on the username you enter.

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
