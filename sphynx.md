Evolution of ALPHV/BlackCat with upgraded capabilities meant to thwart defensive measures

Sphynx differs from the previous variants in notable ways. For example, the command line arguments have been reworked. 
Previous variants utilized the –access-token parameter in order to execute. The updated ransomware removes that parameter and adds a set of more complex arguments. 
This makes it harder to detect since defenders do not have standard commands to hunt.
Additionally, the configuration data is not JSON formatted, but raw structures. Updated samples contain junk code and thousands of encrypted strings which hinder static analysis.  
An announcement by the BlackCat group suggests the motives for updating the ransomware, indicating that BlackCat ransomware “has been completely rewritten from scratch” and that “The main priority of this update was to optimize detection by AV/EDR.” [1]


Encrypts files with AES or ChaCha20 ciphers [2]


[1] https://securityintelligence.com/posts/blackcat-ransomware-levels-up-stealth-speed-exfiltration/
[2] 
