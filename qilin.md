# Qilin

Ransomware affiliates associated with the Qilin ransomware-as-a-service (RaaS) scheme earn anywhere between 80% to 85% of each ransom payment, according to new findings from Group-IB.

Qilin, also known as Agenda, was first documented by Trend Micro in August 2022, starting off as a Go-based ransomware before switching to Rust in December 2022.

The adoption of Rust is also significant not only because of evasion detection capabilities, but also for the fact that it allows the threat actors to target Windows, Linux, and VMware ESXi servers.

The ransomware appears to  use ChaCha20 encryption. It encrypts the randomly generated key along with a file verification hash using RSA-OAEP and appends the data to the encrypted file.

sources:  
[1] https://www.group-ib.com/blog/qilin-ransomware/  
[2] https://thehackernews.com/2023/05/inside-qilin-ransomware-affiliates-take.html  
