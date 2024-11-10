# Cybersecurity DDoS Attack Analysis Project: NST CSF 

## Project Overview

This project is part of my coursework for the **Google Cybersecurity Professional Certificate**. In my capacity as a cybersecurity analyst at a multimedia company that offers web design, graphic design, and social media marketing services to small businesses, I am responsible for analyzing a recent security incident. Our organization faced a Distributed Denial of Service (DDoS) attack, which significantly impacted our internal network services.

This report leverages the National Institute of Standards and Technology's Cybersecurity Framework (NIST CSF) to evaluate the incident thoroughly and propose enhancements to our network security protocols. By doing so, I aim to foster improved communication with stakeholders and bolster our cybersecurity defenses.

## Supporting Document

- [Applying the NIST CSF](https://docs.google.com/document/d/15yCDbDCOAcJw-LTz2DeCA7UeLRfvsf176T6MA6ku6ok/template/preview)

---

## Summary

The organization experienced a significant disruption when all network services became unresponsive. Upon investigation, our cybersecurity team determined that the incident was caused by a DDoS attack involving a surge of incoming ICMP packets. In response, the team acted swiftly to block the attack and temporarily suspend all non-critical network services, allowing us to restore critical functions.

## Identify

The DDoS attack was executed by one or more malicious actors using an ICMP flood strategy. The attack impacted our entire internal network, necessitating the urgent securing and restoration of all critical resources to ensure operational continuity.

## Protect

In the wake of the incident, the cybersecurity team implemented several protective measures, including:

- **New Firewall Rules**: A firewall rule was established to limit the influx of ICMP packets, thereby mitigating the risk of similar attacks in the future.
- **IDS/IPS Deployment**: An Intrusion Detection and Prevention System (IDS/IPS) was installed to filter out ICMP traffic that exhibited suspicious characteristics.

## Detect

To enhance our detection capabilities, the cybersecurity team took the following actions:

- **Source IP Address Verification**: The firewall was configured to verify source IP addresses for any signs of spoofing in incoming ICMP packets.
- **Network Monitoring Software**: We implemented advanced monitoring tools to identify abnormal traffic patterns in real-time, facilitating quicker responses to potential threats.

## Respond

For any future security incidents, our response strategy will include:

- **System Isolation**: Immediate isolation of affected systems to prevent further network disruptions.
- **Critical Service Restoration**: Efforts will be prioritized to restore any critical systems and services impacted by the incident.
- **Post-Incident Analysis**: Network logs will be scrutinized to identify any suspicious or abnormal activities, and a report will be generated for upper management and relevant legal authorities when necessary.

## Recover

In recovering from a DDoS attack triggered by ICMP flooding, the following steps will be executed:

1. **Restoration of Services**: Access to network services will be restored to their normal operational state.
2. **Blocking Future Attacks**: Future external ICMP flood attacks will be mitigated through updated firewall configurations.
3. **Prioritization of Services**: All non-critical network services will be temporarily halted to minimize internal traffic, focusing first on restoring critical services.
4. **Reinstating Non-Critical Services**: Once the flood of ICMP packets has subsided, non-critical systems and services will be gradually brought back online.

---

## Reflections/Notes

This incident underscores the importance of having robust security measures in place and the necessity for a proactive approach to cybersecurity. Moving forward, ongoing training and awareness initiatives will be critical in empowering our staff to recognize and respond to potential threats effectively.
