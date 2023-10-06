# Memory challenges
Solve Using Volatility.
https://www.youtube.com/watch?v=3xeU8U6kUhw&t=156s

* Get imageinfo
> volatility -f flounder-pc-memdump.elf imageinfo

* Confirm profile
> volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 pslist

* Do file scan  
> volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 filescan > out.txt

* Dump file from memory
> volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 dumpfiles -Q fileoffsetfoundusingfilescan -D .

* Get environment variables
> volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 envars

* Dump file from memory
> volatility -f TrueSecrets.raw --profile=Win7SP1x86_23418 dumpfiles --physoffset=0x000000000bbf6158 -u -n -D .

* Dump truecrypt passphrase
> volatility -f TrueSecrets.raw --profile=Win7SP1x86_23418 truecryptpassphrase

* Get command line history
> volatility -f TrueSecrets.raw --profile=Win7SP1x86_23418 cmdscan
> volatility -f TrueSecrets.raw --profile=Win7SP1x86_23418 consoles

# WORD Document

Analyze traffic going from word document after opening it and dump macro content
https://www.youtube.com/watch?v=4UzHNuhTJbs&list=PLUrAjkLbvTpLJGPdxueL5uRvUVwmr4SnY
https://0xv1n.github.io/posts/emo/

* Open document file online
> https://any.run

# Decrypt DES
https://devtoolcafe.com/tools/des

# Tool to extract passwords from firefox profiles

**Firefox Decrypt**

```
firefox_decrypt Firefox
```

**RDP BMC FILE**
use bmc-tool to extract bitmap from the cache file
```
bmc-tools.py -s cache.bin -d bmps
```

Combine all bitmap tiles
```
bmc-toools -s cache.bin -d bmps -b
```

Registry files:
signature: reg

Use registry viewer to view the registry
Look at the startup program
software->microsoft->windows->versions->Run


# event chainsaw
https://github.com/jon-brandy/hackthebox/blob/main/Categories/Forensics/Packet%20Cyclone/README.md
.\chainsaw\chainsaw.exe hunt .\Logs\ -s .\sigma_rules\ --mapping .\chainsaw\mappings\sigma-event-logs-all.yml -o chainsaw-result.txt


# recover python code from executable
```
pyinstxtractor.py binaryname
pycdc program.pyc
```

WMI
https://github.com/davidpany/WMI_Forensics


# Analyze (lsas) memory dump
```
pypykatz lsa minidump 3858793632.pmd
```

Decrypting SMB3 traffic
https://medium.com/maverislabs/decrypting-smb3-traffic-with-just-a-pcap-absolutely-maybe-712ed23ff6a2


# Docker
* Retrieve a file which has been deleted while builiding the image
https://unix.stackexchange.com/questions/499713/how-to-retrieve-a-file-that-has-been-added-then-removed-in-a-docker-image
```
for i in $(sudo ls /var/lib/docker/overlay2/); do sudo ls /var/lib/docker/overlay2/$i/diff/usr/share/lib/librs.so; done
```
