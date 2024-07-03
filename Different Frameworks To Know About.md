NIST 800-53

NIST 800-53 is a set of rules to help organizations keep their information safe. It provides a list of security practices to protect data and systems, like controlling access, monitoring activity, and responding to incidents. It helps organizations manage risks and follow security standards. One example of a security practice is incident response, or IR. We can use this control to combat a compromised network. NIST 800-53 suggests that we follow this plan when dealing with a compromised network:

Preparation: The organization has an incident response policy, trained personnel, and an incident response plan in place.

Detection and Analysis: Security monitoring tools detect unusual activity, and the incident response team analyzes the incident to determine its scope and impact.

Containment: The team isolates affected systems to prevent the malware from spreading further.

Eradication: The team removes the malware from the infected systems and ensures no traces are left.

Recovery: The team restores affected systems to normal operation and monitors them for any signs of recurring issues.

Post-Incident Activity: The incident is documented, and a report is created. The incident response plan is reviewed and updated based on lessons learned.



Cyber Kill Chain

The Cyber Kill Chain is basically a list of steps that threat actors normally take and how to defend against those attacks. These steps include:

Reconnaissance: The attacker gathers information about the target. 

Weaponization: The attacker creates a malicious payload. 

Delivery: The attacker sends the payload to the target. 

Exploitation: The payload exploits a vulnerability in the target system. 

Installation: Malware is installed to maintain access. 

Command and Control (C2): The attacker establishes remote control over the malware. 

Actions on Objectives: The attacker achieves their goal, such as stealing data or disrupting operations.


How we fight this is by:

Reconnaissance: Monitor for unusual scanning or access. 

Weaponization: Block known exploit tools and techniques. 

Delivery: Use email and web filtering to block malicious payloads. 

Exploitation: Keep systems patched and educate users on phishing. 

Installation: Use malware detection and endpoint protection tools. 

Command and Control (C2): Monitor and block suspicious network traffic. 

Actions on Objectives: Implement data loss prevention and security controls.




MITRE ATT&CK

MITRE ATT&CK goes over different tactics, techniques, and procedures that threat actors use to deploy.

An example of MITRE ATT&CK would be:

Tactic: Initial 

Access Technique: Phishing 

Sub-technique: Spear Phishing Attachment 

Procedure: An adversary sends a targeted email with a malicious attachment to gain access to a system.

This is great for knowing how the bad guy thinks and sharpening our red-teaming skills. We can use this in security operations by refining our detection rules and playbooks to align with well-known techniques.




ISO 27001

ISO 27001 focuses more on the management side of information security. It helps organizations protect data through risk management, emphasizing security policies, and adhering to regulations and compliance rules. Companies can actually get certified for this by passing an audit. Normally, a company conducts an internal audit to determine where they are, and they review the ISMS to make sure it aligns with their business objectives. Then an external auditor is brought in to try to pass certification.
