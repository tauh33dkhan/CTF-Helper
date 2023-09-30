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

# WORD Document

Analyze traffic going from word document after opening it and dump macro content
https://www.youtube.com/watch?v=4UzHNuhTJbs&list=PLUrAjkLbvTpLJGPdxueL5uRvUVwmr4SnY
https://0xv1n.github.io/posts/emo/

* Open document file online
> https://any.run

# Decrypt DES
https://devtoolcafe.com/tools/des
