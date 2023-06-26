# BlackCat a.k.a ALPHV a.k.a Noberus

language: Written in Rust (switched in 2022)
encryption: ChaCha20 and AES

platforms: Windows, EXSI, Debian, ReadyNAS, and Synology operating systems

targeting: organizations in the healthcare, government, education, manufacturing and hospitality sectors.


The ransomware also offered two encryption algorithms (ChaCha20 and AES), as well as four encryption modes - Full, Fast, DotPattern and SmartPattern. Full is the most secure but also the slowest mode. SmartPattern offers encryption of “N” megabytes in percentage increments. By default, it encrypts with a strip of 10 megabytes every 10 percent of the file starting from the header, which would be an optimal mode for attackers in terms of speed and cryptographic strength.

Attackers automated the data exfiltration portion of the operation using **ExMatter**, a custom malware capable of ‘melting’ (self-deletion).


The ransomware being deployed by different affiliates can sometimes explain the different TTPs and attack chains used in Noberus attacks.
Use of GPO to spread the malware

For example, threat actors may attempt to increase the speed of their operations by changing default Group Policy refresh times, likely to shorten the window of time between changes taking effect and defenders being able to respond.

sources:  
[1] https://securityintelligence.com/posts/blackcat-ransomware-levels-up-stealth-speed-exfiltration/
