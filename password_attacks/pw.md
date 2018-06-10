# wordlists
http://packetstormsecurity.com/Crackers/
http://www.openwall.com/wordlists/
`/usr/share/john/password.lst`

## ceWL

custom wordlist generator
`cewl -w bulbwords.txt -d 1 -m 5 www.bulbsecurity.com `

## crunch

`crunch 7 7 AB`

## Hydra

`hydra -l georgia -P passwordfile.txt example.com pop3`

`hydra -L userlist.txt -P passwordfile.txt example.com pop3`

`hydra -L userlist.txt -P passwordlist.txt ssh://example.com`

## NT / NTLM Hash

* LM Hash - up to Windows NT
* LM Hash and NTLM Both - Windows XP
* NTLM Only - Windows 7 +

### LM Hash

* Truncated at 14 characters.
* All uppercase.
* Fewer than 14 characters are null-padded.
* The 14-character password is broken into two seven-character passwords that are hashed separately.

Hash of empty value (7chars)
> AAD3B435B51404EEAAD3B435B51404EE
> AAD3B435B51404EE

* SAM file is encrypted with 128-bit Rivest Cipher 4 (RC4)
* Encryption key for the `Syskey` utility is called the `bootkey` (stored in the Windows SYSTEM file)

### Extract `bootkey`

`windows/repair/system`
`bkhive system xpkey.txt`

### Extract hashes

`meterpreter > hashdump`
`windows/system32/config/sam`
`windows/repair/sam`
`samdump2 sam xpkey.txt`

### John the Ripper

john xphashes.txt
/etc/john/john.conf
   List.Rules:Wordlist
--rule

### Windows Credential Editor (WCE)

* Pull from Local Security Authority Subsystem Service (LSASS)
   * Process in charge of enforcing the system’s security policy

## Wordpress password

`php> echo password_hash('example', PASSWORD_DEFAULT);`


# Decrypt encrypted RSA keys

sshng2john id_rsa
john / jumbojohn

# Decrypt cyphers

https://www.quipqiup.com/

# Create password hash for linux

`openssl passwd -1 -salt password`
