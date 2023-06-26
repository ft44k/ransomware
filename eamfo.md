At least one affiliate of the Noberus ransomware operation was spotted in late August (2022) using information-stealing malware that is designed to steal credentials stored by Veeam backup software. Veeam is capable of storing credentials for a wide range of systems, including domain controllers and cloud services. The credentials are stored to facilitate the backup of these systems.


The malware (Infostealer.Eamfo) is designed to connect to the SQL database where Veeam stores credentials, and it steal credentials with the following SQL query:

select [user_name],[password],[description] FROM [VeeamBackup].[dbo].[Credentials]

Eamfo will then decrypt and display the credentials.
