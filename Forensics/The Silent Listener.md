*You're connected to a simulated internal company network. Rumor has it that an intern accidentally left a sensitive data exposed.*

Attachments:

Data.pcap

One of the packet contains a .zip file in hex

![[Pasted image 20250613094542.png]]

When trying the to unzip, a password is required. Use john / hashcat to bruteforce the password.
The password comes out to be letmein

![[Pasted image 20250613193942.png]]

Flag
`flag{http_exfiltration_detected}`



