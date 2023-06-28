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

## Capability

### Resource Development

| [T1587.001](https://attack.mitre.org/techniques/T1587/001/)| Written in Goland targeting Windows only |
| [T1583.001](https://attack.mitre.org/techniques/T1583/001/) |BianLian shares victim information on a TOR leak site |

| Initial Access|-|
| ------ | ------ |
| [T1021.001](https://attack.mitre.org/techniques/T1021/001/)| Exploits RDP protocol to infect victims|
| [T1190](https://attack.mitre.org/techniques/T1190/) |BianLian exploits ProxyShell or vulnerable SonicWall VPN |

| Execution|-|
| ------ | ------ |
| [T1059.003](https://attack.mitre.org/techniques/T1059/003/)| BianLian uses Windows Command Shell to execute certain functions|

| Defense Evasion|-|
| ------ | ------ |
| [T1562.009](https://attack.mitre.org/techniques/T1562/009/)| BianLian boots Windows servers in safe mode to remain undetected|
| [T1070.004](https://attack.mitre.org/techniques/T1070/004/)| BianLian removes itself from the device when encryption is done|
| [T1497](https://attack.mitre.org/techniques/T1497/)| BianLian uses certain API calls to attemtp to confuse/crash sandboxes|
| [T1497.001](https://attack.mitre.org/techniques/T1497/001/)| BianLian checks if it runs via WINE|


[1] https://decoded.avast.io/threatresearch/decrypted-bianlian-ransomware/  
[2] https://www.bleepingcomputer.com/news/security/bianlian-ransomware-gang-shifts-focus-to-pure-data-extortion/  
[3] https://redacted.com/blog/bianlian-ransomware-gang-continues-to-evolve/  
