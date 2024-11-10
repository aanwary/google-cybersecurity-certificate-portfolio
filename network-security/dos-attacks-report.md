# Cybersecurity Incident Report: DoS Attacks

This report is part of my coursework for the **Google Cybersecurity Professional Certificate**. In this assignment, I analyze a network security incident involving a **Denial of Service (DoS)** attack on a travel agency's website. Using server logs, I identify the type of attack and explain its impact on the system’s functionality.

## Supporting Documents

- [Incident Report Template](https://docs.google.com/document/d/1xEk_arFwlQOto7KEM6gN-sIYriXhP9-lY2ftpBXhS4M/template/preview?resourcekey=0-_ODneeo__mDgK7BTE1FkVA)
- [Wireshark TCP/HTTP Log](https://docs.google.com/spreadsheets/d/1enpRzrIao3J2Lp2tOI0hmu1Cu7D7CjLGhFAiTiR9J64/edit?gid=218501934#gid=218501934)

These documents were utilized to complete this report and provide further insight into network intrusion analysis.

---

## Cybersecurity Incident Report

### Section 1: Identify the type of attack that may have caused this network interruption

The likely cause of the website’s connection timeout error is a **Denial of Service (DoS)** attack. A review of the logs revealed that the server stopped responding after a surge in SYN packet requests from an unfamiliar IP address. This pattern aligns with a **SYN Flood Attack**, a specific type of DoS attack where the server’s resources are overwhelmed by numerous partially open connections that remain uncompleted.

---

### Section 2: Explain how the attack is causing the website to malfunction

When users attempt to connect to a web server, a **three-way handshake** process in the TCP protocol is followed:

1. The client sends a **SYN packet** to the server, initiating the connection.
2. The server responds with a **SYN-ACK packet**, reserving resources and acknowledging the connection request.
3. The client completes the handshake by replying with an **ACK packet**, establishing the connection.

In the scenario of a SYN Flood Attack, an attacker sends numerous SYN packets but does not complete the handshake, consuming server resources by maintaining multiple half-open connections. This resource exhaustion prevents legitimate connections from being established, leading to connection timeouts for users attempting to access the site.

The logs indicate that the server has been overwhelmed with incomplete SYN requests, which hinders its ability to respond to legitimate traffic and results in service disruptions for users.
