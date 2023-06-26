Cl0p ransomware emerged in 2019 and is associated with the TA505 [1] which is the group behind Dridex and Locky Ransomware. /aka INDRIK SPIDER/


Malware is written in C, encrypts files stored locally, if directed encrypts files stored on network shares, some variants may also delete volume shadow copies


Cl0p.linux
built for linux environments that is capable of enumerating files within system and software directories to encrypt their content using RC4 symmetric encryption

Targeting: large companies in financial, healthcare, manufacturing, media, but it was seen to tager also small and medium businesses


Clop encrypts files using combination of AES-256, RSA and RC4, encryption keys are then stored on a remote server.

It has capabilities to spread itself via network, meaning it can infect multiple machines at once.


[1] https://www.sentinelone.com/labs/labscon-replay-star-gazing-using-a-full-galaxy-of-yara-methods-to-pursue-an-apex-actor/  
[2] https://malpedia.caad.fkie.fraunhofer.de/actor/ta505  
[3] https://malpedia.caad.fkie.fraunhofer.de/details/elf.clop  
