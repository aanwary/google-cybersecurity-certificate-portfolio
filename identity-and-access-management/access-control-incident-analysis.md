# Access Control Incident Analysis: User Deprovisioning 

---

## Incident Summary

A recent payroll-related incident involved an unauthorized deposit to an unknown bank account, which was later halted. This incident prompted an investigation to identify gaps in the company’s access control practices and secure business operations going forward.

---

## Notes on the Incident

- **Event Date**: October 3, 2023  
- **User Role**: Legal/Administrator  
- **Login IP**: 152.207.255.255  

The event log shows that the account was accessed on this date, using an IP address outside the normal range, suggesting that the user may have accessed the system from an unauthorized or unknown network.

---

## Identified Access Control Issues

1. **Expired Contractor Access**  
   The payroll system was accessed by Robert Taylor, Jr., a former contractor with administrative permissions whose contract ended in 2019. However, his account remained active and retained high-level access in 2023, pointing to a lack of regular account audits and expiration policies for inactive accounts.

2. **Use of Shared Accounts**  
   Employees currently manage shared resources using a single, shared cloud account. This setup limits individual accountability and makes it challenging to track specific user actions within the system, creating potential security and tracking gaps.

---

## Recommended Access Control Improvements

1. **Implement Account Expiration Policies**  
   Set accounts to automatically expire 30 days after a contractor’s or employee’s role ends, particularly for high-access and administrative accounts. This would prevent inactive accounts from being exploited long after a user has left the company.

2. **Enforce Unique User Accounts with Role-Based Access Control (RBAC)**  
   Instead of shared accounts, assign each employee a unique account with permissions limited to their role’s requirements. This way, actions are traceable to individuals, and permissions can be limited to only necessary functions, improving accountability.

3. **Enable Multi-Factor Authentication (MFA)**  
   Require multi-factor authentication (MFA) for all logins, especially for remote access and administrative accounts. MFA would add a layer of security by requiring additional identity verification, making unauthorized access significantly harder.

---

## Conclusion

This incident illustrates the importance of stringent access controls, such as account expiration, individual user accounts, and multi-factor authentication. Implementing these measures will mitigate unauthorized access risks and enhance security for sensitive systems.
