# windows-security-assessment
1. Antivirus Baseline

- Antivirus solution: McAfee (third-party)
- Status: No action needed
- Windows Defender: Managed by third-party antivirus
- Observation: System relies on third-party AV for real-time protection

2. Firewall Baseline

- Domain network firewall: ON (No action required)
- Private network firewall: ON (No action required)
- Public network firewall: ON (No action required)
- Observation: Windows Defender Firewall is enabled across all network profiles.

3. User Account Baseline

- Total number of user accounts: 1
- Account type: Administrator + User
- Authentication method: Microsoft account (email-based login)
- Observation: Single administrator account used for daily activities. If compromised, attacker would gain full system-level access.

4. App & Browser Control Baseline

- Reputation-based protection: OFF
- Observation: System does not currently block apps/files based on Microsoft’s cloud reputation.
- Threat: Malicious or untrusted apps may run undetected.

5. Threat Modeling / Attack Surface

- Single admin account increases risk if compromised.
- Public Wi-Fi usage may allow network attacks.
- Third-party AV dependency; zero-day threats possible.
- Outdated or vulnerable applications may be exploited.
- Key threats considered: credential theft, malware persistence, unauthorized access.

6. Hardening — Antivirus (Periodic Scanning)
- Periodic scanning: Enabled
- Observation: Windows Defender will perform additional scans alongside McAfee, providing layered protection.
- Windows Update: Enabled
- Observation: System receives security patches regularly, reducing vulnerability risk.

6b. Hardening — Reputation-based Protection

- Action: Enabled Reputation-based protection in App & Browser Control
- Observation: System now blocks untrusted apps/files based on Microsoft’s cloud reputation.
- Benefit: Reduces risk of malicious or untrusted applications running undetected.


7. Admin Account Hardening

- Sign-in method: Microsoft account with PIN / password
- Observation: Strong authentication reduces risk of unauthorized access.

7b. Admin Account Hardening — Standard Daily User

- Created a separate standard user account: Daily User
- Admin account will only be used for system changes
- Observation: Separating admin from daily use reduces risk of full system compromise

8. Final Security Posture Summary

Before Hardening:
- Reputation-based protection was disabled.
- Single administrator account used for daily activities.
- Limited layered protection due to reliance on third-party AV alone.

After Hardening:
- Reputation-based protection enabled to block untrusted apps.
- Layered security achieved using both McAfee and Defender periodic scanning.
- Separation of admin and daily user accounts reduces risk of full system compromise.

Overall Impact:
- Reduced malware execution risk.
- Reduced privilege escalation impact.
- Improved defense-in-depth on a Windows system.


