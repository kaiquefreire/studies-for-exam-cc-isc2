# Data Handling
- Here we will summarize the data Life Cycle

| Lifecycle | Description |
|----------------|---------------|
| Create| Creating the knowledge, which is usually tacit knowledge at this point. |
| Store | Storing or recording it in some fashion (which makes it explicit). |
| Use   | Using the knowledge, which may cause the information to be modified, supplemented or partially deleted.|
| Share | Sharing the data with other users, whether as a copy or by moving the data from one location to another. |
| Archive | Archiving the data when it is temporarily not needed. |
| Destroy | Destroying the data when it is no longer needed. |

## Practices
| Concept | Definition |
| --- | --- | 
| Classification | Businesses recognize that information has value and others might steal their advantage if the information is not kept confidential, so they classify it.  |
| Labeling | Security labels are part of implementing controls to protect classified information. It is reasonable to want a simple way of assigning a level of sensitivity to a data asset, such that the higher the level, the greater the presumed harm to the organization, and thus the greater security protection the data asset requires. | 
| Retention | Information and data should be kept only for as long as it is beneficial, no more and no less.  |
| Destruction | Data that might be left on media after deleting is known as remanence and may be a significant security concern. |

# Logging and Monitoring Security Events
**Ingress monitoring** refers to surveillance and assessment of all inbound communications traffic and access attempts. **Some tools include**:

- Firewalls
- Gateways
- Remote Authentication Servers
- IDS/IPS Tools
- SIEM solutions
- Anti-malware solutions

**Egress monitoring** is used to regulate data leaving the organization’s IT environment. The term currently used in conjunction with this effort is data loss prevention (DLP) or data leak protection. The **DLP solution should be deployed so that it can inspect** all forms of data leaving the organization, including: 

- Email
- Copy to portable media
- File transfer protocol (FTP)
- Posting to web pages/websites
- Applications/application programming interfaces (APIs) 

# Encryption & Cryptography
- **Encryption** protects our personal and business transactions; digitally signed software updates verify their creator’s or supplier’s claim to **authenticity**. 
- **Cryptography** is used to protect information by keeping its meaning or content secret and making it unintelligible to someone who does not have a way to decrypt (unlock) that protected information. 

Let associate the security principles to this concepts:
- **Encryption:** Authenticity
- **Cryptography:** Confidentiality and Integrity

## Symmetric Encryption & Assymetric 

| Cryptography Type | Definition | Simple real example | Use Cases
| --- | --- | --- | --- |
| Symmetric Encryption | A type of encryption in which the same key is used for both encrypting and decrypting the data. | A lock that uses the same key to lock and unlock a door. | Encrypting bulk data (backups, hard drives, portable media), Encrypting messages traversing communications channels (IPsec, TLS), Streaming large-scale, time-sensitive data (audio/video materials, gaming, etc.) |
| Asymmetric Encryption | A type of encryption that uses a distinct pair of keys, one public and one private, for encrypting and decrypting the data. | A mailbox in which anyone can put a letter (public key) in it, but only the owner of the mailbox can open (using their private key) and read the letters that have been left there. | VPNs, Certificates SSL/TLS, SFTP. |

## Configuration Management
Is a process and discipline used to ensure that the only changes made to a system are those that have been authorized and validated.

- Identification: Baseline identification of a system and all its components, interfaces and documentation.
- Baseline: A security baseline is a minimum level of protection that can be used as a reference point. Baselines provide a way to ensure that updates to technology and architectures are subjected to the minimum understood and acceptable level of security requirements. A set of security controls or system settings used to ensure uniformity of configuration throughout the IT environment.
- Change Control: An update process for requesting changes to a baseline, by means of making changes to one or more components in that baseline. A review and approval process for all changes. This includes updates and patches. 
- Verification and Audit: A regression and validation process, which may involve testing and analysis, to verify that nothing in the system was broken by a newly applied set of changes. An audit process can validate that the currently in-use baseline matches the sum total of its initial baseline plus all approved changes applied in sequence.