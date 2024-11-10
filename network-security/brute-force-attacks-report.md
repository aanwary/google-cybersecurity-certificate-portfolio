# Cybersecurity Incident Report: Brute Force Attacks

This report is part of my coursework for the **Google Cybersecurity Professional Certificate**. This report documents a security incident involving the website **yummyrecipesforme.com** that was compromised through a brute force attack, leading to the installation of malware on visitors' devices.

## Supporting Documents

- **TCPDUMP Traffic Log**: [View TCPDUMP Log](https://docs.google.com/document/d/1HDAQTLSK5CyPLPHeLI0s75kNE-kA2kG0NFJoZlz0xCc/template/preview?resourcekey=0-vDSHnW4qKxOOQtsZeGRUeQ)
A
## Section 1: Identify the Network Protocol Involved in the Incident

The primary network protocol involved in the incident is the **Hypertext Transfer Protocol (HTTP)**. The incident was related to the web server for **yummyrecipesforme.com**, where requests for web pages are communicated over HTTP traffic. The tcpdump log captures demonstrate the utilization of the HTTP protocol during the interactions with the website. Specifically, the malicious file was transmitted to users’ computers over this protocol at the application layer.

During the investigation, the tcpdump log revealed that the initial request was sent to the DNS server to resolve the IP address for yummyrecipesforme.com. After the DNS provided the correct IP address, the browser directed users to the website. The scenario states that upon loading the website, visitors were prompted to download a file that would supposedly give them access to free recipes. This activity occurred via HTTP, which is part of the application layer of the TCP/IP model. Furthermore, after downloading the file, the logs indicated that the browser made a subsequent request to the DNS server for the address of **greatrecipesforme.com**, ultimately redirecting users to this malicious site using HTTP.

## Section 2: Document the Incident

Several customers contacted the helpdesk at yummyrecipesforme.com reporting that they were prompted to download and execute a file while visiting the website, claiming it provided access to new recipes. After running the file, customers noted that their computers began to operate slowly. In response to these reports, the website owner attempted to log into the web server but discovered that they were locked out of their administrative account.

To investigate, the cybersecurity analyst created a sandbox environment to safely access the website without affecting the company’s network. Using tcpdump, the analyst captured the network traffic generated during the interaction with the website. Upon accessing the site, the analyst was prompted to download a file that promised free recipes, which they accepted and executed. The result was a redirection to a fraudulent website, **greatrecipesforme.com**.

The analyst reviewed the tcpdump log, noting the browser's initial request for the IP address associated with **yummyrecipesforme.com**. Once the connection was established over HTTP, the analyst documented the download and execution of the file. The logs illustrated a shift in network traffic as the browser then requested a new IP address for **greatrecipesforme.com**, indicating the redirection of users to this malicious site.

The senior cybersecurity analyst subsequently examined the source code of both websites and the downloaded file. It was confirmed that the attacker had inserted code into the original site, prompting users to download a malicious file disguised as a browser update. The investigation revealed that the website owner had been locked out due to the attacker successfully executing a brute force attack, enabling them to change the admin password. Consequently, the execution of the malicious file compromised users’ computers.

## Section 3: Recommend One Remediation for Brute Force Attacks

To protect against future brute force attacks, the team recommends implementing **two-factor authentication (2FA)** for all administrative accounts. This additional layer of security requires users to provide two forms of identification before gaining access to their accounts, significantly enhancing protection against unauthorized access.

**Rationale**: 
1. **Increased Security**: 2FA effectively mitigates the risks posed by compromised passwords. Even if an attacker successfully guesses the admin password, they would still require a second factor, such as a one-time code sent to the user’s phone or email, to gain access.
2. **Risk Mitigation**: By requiring both something the user knows (a password) and something the user has (the 2FA device), the likelihood of a successful brute force attack is greatly diminished. This makes it significantly more difficult for an attacker to access sensitive information and administrative functions.

In addition to 2FA, it is advisable to enforce strong password policies, including disallowing the reuse of previous passwords and implementing longer password requirements. This further secures administrative accounts against brute force attacks and enhances overall network security.
