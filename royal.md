# Royal

The Royal ransomware group has targeted over 1,000 organizations with a social engineering attack, tricking victims into trusting the attackers. The scheme involves pressuring victims to open a file that is actually a malware loader. If successful, victims can fall victim to ransomware. 

The group may have even created a fake version of the Midnight Group to further deceive victims. This variation of a gambit known as BazarCall involves scaring victims into thinking their systems have been locked by ransomware and manipulating them into installing the actual ransomware. 

Royal is a ransomware group splintered from Conti after backing the Kremlin’s war on Ukraine. The group targets healthcare companies and top-tier corporations for ransom demands ranging from $250,000 to over $2 million. They use BazarCall strategies and have recently targeted Linux systems. Their encryption scheme is implemented correctly, making recent backups or a decryptor the only way to recover lost files.


Royallocker (Royal)

platform: windows

capabilities: encryption of local files, disabling running processes, deleting shadow copies, encryption of vmdk files


royallocker.linux
platform: linux

written in C and built for Linux systems that features cross-compilation elements from its Windows version.
The malware leverages the OpenBSD library that contains cryptography functions, which are used to encrypt file contents using AES-256 in CBC

The code family is designed to execute on Linux and VMKernel

Sources:
[1] https://gridinsoft.com/blogs/conti-ransomware-2023/
