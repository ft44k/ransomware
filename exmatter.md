## Exmatter

tool use for data exfiltration.

The latest version of Exmatter has reduced the number of file types it attempts to exfiltrate. It will now exfiltrate files with the following extensions only:

`.pdf, .doc, .docx, .xls, .xlsx, .png, .jpg, .jpeg, .txt, .bmp, .rdp, .txt, .sql, .msg, .pst, .zip, .rtf, .ipt, .dwg``


exfiltration capability FTP, SFTP and WebDav,

Whether Exmatter is the creation of Coreid or a skilled affiliate of the group is not clear, but its use alongside two different iterations of Coreid’s ransomware is notable.


ExMatter is exclusively used by one **BlackCat** ransomware affiliate cluster, tracked by Microsoft as DEV-0504. [1]



Exmatter is a .NET data exfiltration tool used in prominent ransomware campaigns (e.g. BlackCat, BlackMatter) to retrieve stolen data before the encryption is completed in the victim's box. The .NET code has been seen obfuscated with ConfuserEx v1.6. 
Exmatter will enumerate logical drives and iterates through the file system excluding a list of directories and searching for certain file sizes and extensions. 
Exmatter prioritizes extraction of recently modified files in an attempt to extract data that is more likely to be of higher interest to the victim. Extracted files have been seen used as bargain during ransom negotiations. Exmatter employs SFTP and webDAV protocols to transfer the data to a remote server using hard-coded credentials. Later versions of Exmatter include a new data corruption feature which corrupts files on disk that have been successfully exfiltrated.[2]



[1] https://securityintelligence.com/posts/blackcat-ransomware-levels-up-stealth-speed-exfiltration/

[2] https://exchange.xforce.ibmcloud.com/malware-analysis/guid:21548b1ad32b8a73b6dbfba639575093?_gl=1*9c05rs*_ga*OTk3MjQ2NDIwLjE2ODY3MTY4MTg.*_ga_FYECCCS21D*MTY4NjcxNjgxOC4xLjEuMTY4NjcxNjkxOS4wLjAuMA..&_ga=2.248315911.1260934385.1686716818-997246420.1686716818
