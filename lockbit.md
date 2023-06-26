# Lockbit

is a prominent Ransomware-as-a-Service (RaaS) affiliate program,  that has been advertised in underground forums since early 2020.

Lockbit is written in C that encrypts files stored localy and on network shares.
It can also identify other systems on a network and propagate via SMB.  
Prior encrypting the files, LOCKBIT clears the event logs, deletes volume shadow copies, and terminates processes and services that may impact its ability to encrypt files.

file extension:  .lockbit

platform: Windows

# Lockbit 2.0
Written in C encrypts files on local drives and mapped network locations using AES-128 and encrypts symetric keys and IVs using Curve25519

This version of Lockbit was propagating via GPOs, SMB and RPC, deleting shadow copies and terminating targeted processes and services prior to encrypting the files.

Platform: Windows

# Lockbit 3.0
language: C

Shares significant portion of code with Blackmatter, including overlaps in anti-analysis, anti-debugging, and API obfuscation code

source: https://www.cisa.gov/news-events/cybersecurity-advisories/aa23-075a
