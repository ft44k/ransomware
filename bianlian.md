# BianLian

is a ransomware strain written in Go language and compiled as a 64-bit Windows executable. Due to the nature of the Go language, there are many strings directly visible in the binary.
File data is encrypted with AES-256 in CBC mode. The length of the encrypted data is aligned to 16 bytes, as required by the AES CBC cipher. 

Upon its execution, BianLian searches all available disk drives (from A: to Z:). For all found drives, it searches all files and encrypts all whose file extension matches one of the 1013 extensions hardcoded in the ransomware binary. 
Interestingly enough, the ransomware doesn’t encrypt the file from the start nor does it encrypt a file to the end. Instead, there is a fixed file offset hardcoded in the binary from which the encryption proceeds. The offset differs per sample, but none of the known samples encrypts data from the start of the file.[1]



They exploit:
-  weak Remote Desktop Protocol 
- proxyshell (exchage vulnerability)


___UPDATE__[16/3/2023]

The BianLian ransomware group has shifted its focus from encrypting its victims' files to only exfiltrating data found on compromised networks and using them for extortion.[2]

Redacted [3] reports that BianLian operators have kept their initial access and lateral movement techniques the same and continue to deploy a custom Go-based backdoor that gives them remote access on the compromised device, albeit a slightly improved version of it.


[1] https://decoded.avast.io/threatresearch/decrypted-bianlian-ransomware/  
[2] https://www.bleepingcomputer.com/news/security/bianlian-ransomware-gang-shifts-focus-to-pure-data-extortion/  
[3] https://redacted.com/blog/bianlian-ransomware-gang-continues-to-evolve/  
