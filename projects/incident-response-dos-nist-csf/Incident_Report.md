# Incident Response Report

## Incident Summary

### Date
Simulated Scenario

### Incident Type
Denial of Service (DoS) - ICMP Flood

### Impact

The organization's internal network became unavailable for approximately two hours due to an ICMP Flood attack. Legitimate users were unable to access internal services because the network infrastructure became overloaded by malicious traffic.

---

# Root Cause Analysis

During the investigation, the cybersecurity team determined that the attacker exploited a misconfigured firewall. The firewall lacked adequate filtering and rate limiting for incoming ICMP traffic, allowing an excessive number of packets to reach the internal network.

The attacker also used spoofed source IP addresses, making the attack more difficult to identify and filter.

---

# NIST Cybersecurity Framework Analysis

## 1. Identify

### Assets Affected

- Firewall
- Internal Network
- Corporate Servers
- Network Services
- Employee Workstations

### Risks Identified

- Firewall misconfiguration
- No ICMP rate limiting
- Lack of continuous monitoring
- No IDS/IPS
- Risk of IP spoofing

### Assessment

The organization's firewall configuration represented the primary security weakness that enabled the attack.

---

## 2. Protect

To reduce the likelihood of future attacks, the following security controls were implemented:

- ICMP rate limiting
- Source IP validation
- Firewall hardening
- Security policy review
- Regular firewall audits
- Administrator awareness training

These measures significantly reduce the attack surface.

---

## 3. Detect

The organization improved its detection capabilities by implementing:

- Network monitoring software
- Intrusion Detection and Prevention System (IDS/IPS)
- Firewall log monitoring
- Traffic baseline analysis
- Automated alerts for abnormal ICMP traffic

These controls allow faster identification of suspicious network activity.

---

## 4. Respond

During the incident, the response team:

- Blocked incoming ICMP traffic
- Disabled non-critical services
- Prioritized critical business services
- Investigated the attack source
- Identified the firewall vulnerability
- Updated firewall rules

The response successfully restored business operations while limiting additional impact.

---

## 5. Recover

Recovery activities included:

- Restoring affected network services
- Deploying the updated firewall configuration
- Validating network stability
- Activating continuous monitoring
- Reviewing incident response procedures

The organization also recommended periodic security assessments to improve resilience against future attacks.

---

# Lessons Learned

This incident demonstrated that improper firewall configuration can expose an organization to denial-of-service attacks.

Applying the NIST Cybersecurity Framework helped structure the organization's response by identifying vulnerabilities, implementing protective controls, improving detection capabilities, strengthening incident response procedures, and ensuring a reliable recovery process.

Future security efforts should focus on proactive monitoring, periodic firewall audits, and continuous improvement of the incident response process.
