# Internal Security Audit: Botium Toys

This project is part of my coursework for the **Google Cybersecurity Professional Certificate**. This project contains an internal security audit for **Botium Toys**, assessing the current security posture of the organization, evaluating existing controls, and examining compliance with relevant standards.

## Overview

- **Company**: Botium Toys
- **Purpose**: To assess the effectiveness of security controls and compliance measures within the IT infrastructure of Botium Toys.
- **Scope**: The entire security program, including physical assets, internal networks, and systems.

## Audit Objectives

1. Identify current assets managed by the IT department.
2. Assess compliance with regulatory standards.
3. Provide recommendations for improving security posture.

## Supporting Documents

- **[Risk Assessment Document](https://docs.google.com/document/d/1s2u_RuhRAI40JSh-eZHvaFsV1ZMxcNSWXifHDTOsgFc/template/preview)**: Overview of risks associated with current security posture.
- **[Control Categories Document](https://docs.google.com/document/d/1HsIw5HNDbRXzW7pmhPLsK06B7HF-KMifENO_TlccbSU/template/preview)**: Detailed descriptions of control categories.
- **[Controls and Compliance Checklist](https://docs.google.com/document/d/10NoXfyE3ZSiHFqiTE0fINL3xdPvTZq0j0VwnFEM0N3g/edit?tab=t.0#heading=h.87tykp1u0l36)**: Checklist used for conducting the security audit.

## Controls and Compliance Checklist

### Controls Assessment

| Control                                      | Yes | No | Explanation                                                                                                     |
|----------------------------------------------|-----|----|-----------------------------------------------------------------------------------------------------------------|
| Least Privilege                              | [ ] | [X] | Currently, all employees have access to customer data; privileges need to be limited to reduce the risk of a breach.|
| Disaster Recovery Plans                      | [ ] | [X] | There are no disaster recovery plans in place. These need to be implemented to ensure business continuity.       |
| Password Policies                            | [ ] | [X] | Employee password requirements are minimal, which could allow a threat actor to more easily access secure data. |
| Separation of Duties                         | [ ] | [X] | Needs to be implemented to reduce the possibility of fraud/access to critical data; CEO manages payroll.       |
| Firewall                                     | [X] | [ ] | The existing firewall blocks traffic based on an appropriately defined set of security rules.                    |
| Intrusion Detection System (IDS)            | [ ] | [X] | The IT department needs an IDS in place to help identify possible intrusions by threat actors.                  |
| Backups                                      | [ ] | [X] | The IT department needs to have backups of critical data, in case of a breach, to ensure business continuity.    |
| Antivirus Software                           | [X] | [ ] | Antivirus software is installed and monitored regularly by the IT department.                                   |
| Manual Monitoring for Legacy Systems         | [ ] | [X] | There is no regular schedule for monitoring legacy systems, placing them at risk of a breach.                    |
| Encryption                                   | [ ] | [X] | Encryption is not currently used; implementing it would provide greater confidentiality of sensitive information.  |
| Password Management System                   | [ ] | [X] | There is no password management system currently in place; implementing this control would improve productivity. |
| Locks (Offices, Storefront, Warehouse)      | [X] | [ ] | The physical location has sufficient locks.                                                                    |
| Closed-Circuit Television (CCTV)            | [X] | [ ] | CCTV is installed and functioning at the store’s physical location.                                            |
| Fire Detection/Prevention Systems            | [X] | [ ] | The physical location has a functioning fire detection and prevention system.                                   |

### Compliance Assessment

#### Payment Card Industry Data Security Standard (PCI DSS)

| Best Practice                                                                         | Yes | No | Explanation                                                                                                      |
|---------------------------------------------------------------------------------------|-----|----|------------------------------------------------------------------------------------------------------------------|
| Only authorized users have access to customers’ credit card information.             | [ ] | [X] | Currently, all employees have access to the company’s internal data.                                            |
| Credit card information is securely accepted, processed, transmitted, and stored.   | [ ] | [X] | Credit card information is not encrypted, and all employees currently have access to it.                         |
| Implement data encryption procedures for credit card transactions.                    | [ ] | [X] | The company does not currently use encryption to ensure the confidentiality of customers’ financial information.  |
| Adopt secure password management policies.                                            | [ ] | [X] | Password policies are nominal, and no password management system is currently in place.                          |

#### General Data Protection Regulation (GDPR)

| Best Practice                                                                         | Yes | No | Explanation                                                                                                      |
|---------------------------------------------------------------------------------------|-----|----|------------------------------------------------------------------------------------------------------------------|
| E.U. customers’ data is kept private/secured.                                        | [ ] | [X] | The company does not currently use encryption to ensure the confidentiality of customers’ financial information.  |
| There is a plan to notify E.U. customers within 72 hours of a data compromise.      | [X] | [ ] | There is a plan to notify E.U. customers within 72 hours of a data breach.                                       |
| Ensure data is classified and inventoried.                                           | [ ] | [X] | Current assets have been inventoried but not classified.                                                        |
| Enforce privacy policies, procedures, and processes.                                  | [X] | [ ] | Privacy policies have been developed and enforced among IT team members and other employees as needed.          |

#### System and Organizations Controls (SOC Type 1, SOC Type 2)

| Best Practice                                                                         | Yes | No | Explanation                                                                                                      |
|---------------------------------------------------------------------------------------|-----|----|------------------------------------------------------------------------------------------------------------------|
| User access policies are established.                                                | [ ] | [X] | Controls of Least Privilege and separation of duties are not currently in place; all employees have access.     |
| Sensitive data (PII/SPII) is confidential/private.                                   | [ ] | [X] | Encryption is not currently used to better ensure the confidentiality of PII/SPII.                              |
| Data integrity ensures the data is consistent, complete, accurate, and has been validated.| [X] | [ ] | Data integrity is in place.                                                                                     |
| Data is available to individuals authorized to access it.                            | [ ] | [X] | While data is available to all employees, authorization needs to be limited to only the individuals who need access. |

## Recommendations

1. **Implement Least Privilege Access**: Restrict access to sensitive data to only those who need it.
2. **Establish Disaster Recovery Plans**: Develop and document a disaster recovery strategy.
3. **Enhance Password Policies**: Implement stronger password complexity requirements and a centralized password management system.
4. **Install an Intrusion Detection System (IDS)**: To monitor network traffic for suspicious activity.
5. **Conduct Regular Backups**: Ensure critical data is regularly backed up and can be restored if needed.

## Conclusion

This audit provides an essential overview of Botium Toys' current security posture and highlights areas for improvement. Implementing the recommendations will help mitigate risks and enhance the overall security framework.
