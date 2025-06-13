
*During the final days of WWII, a rogue German engineer modified the standard Enigma cipher to secure a personal transmission. The intercepted message looks like normal Enigma output — but standard decryption methods yield garbage.Your mission: decrypt the message and recover the buried location.

Intercepted Ciphertext:
64 6e 4e 7a 63 48 55 67 62 32 4a 30 61 47 38 67 59 6d 31 71 61 32 63 67 61 57 70 6a 5a 6e 45 67 63 58 56 6a 64 57 45 67 65 57 31 70 63 57 34 67 62 57 74 75 62 57 6f 67 5a 51 3d 3d

On decoding the given hex dump we get base64 :

dnNzcHUgb2J0aG8gYm1qa2cgaWpjZnEgcXVjdWEgeW1pcW4gbWtubWogZQ==

On decoding the base64:

vsspu obtho bmjkg ijcfq qucua ymiqn mknmj e

Now the challenge prompt talks about ww2 and enigma but this is non-standard enigma. Bruteforcing all settings and models can be arduous. There is a .zip file attached with the challenge which is password protected.

The password of the zip file is the name of one of the first people to crack enigma - Alan Mathison Turing.

On entering alanmathisonturing, we get

![image](Pasted%20image%2020250613104643.png)

The file has the settings and model name for the decrypting the ciphertext.


![image](Pasted%20image%2020250613105514.png)

Flag

`flagt hefla gisin theca vebeh indth eruin s`
`flagtheflagisinthecavebehindtheruins`
`flag{theflagisinthecavebehindtheruins}`