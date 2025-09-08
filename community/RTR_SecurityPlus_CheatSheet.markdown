# RTR CompTIA Security+ Cheat Sheet
**Estimated Duration**: 15 minutes  
**Purpose**: This cheat sheet, crafted by Recognize The Real Tech (RTR), prepares Little Rock SMBs and community members, especially Black talent, for the CompTIA Security+ certification. It supports RTR’s mission to empower businesses with affordable IT solutions and uplift communities through education. Use this guide for RTR’s free quarterly workshops or as a client resource for RTR’s “RTR Shield” cybersecurity services.

## What You’ll Learn
- Understand the five CompTIA Security+ exam domains and their relevance to securing local businesses.  
- Identify free/low-cost tools for hands-on practice, tailored to RTR’s managed IT and cybersecurity services.  
- Access a structured study plan and local resources (e.g., ASBTDC, Rock It! Lab) to pass the exam.  
- Prepare for performance-based questions (PBQs) with practical tasks aligned with RTR’s automation and consulting offerings.

## Exam Domains and RTR Applications
### 1.0 General Security Concepts (12%)
**Core Knowledge**: Foundational security principles for protecting SMBs.  
**RTR Relevance**: Guides RTR’s cybersecurity audits ($500-1K/project) and client education.  
- **1.1 Security Controls**:  
  - **Categories**: Technical (e.g., firewalls), Managerial (e.g., policies), Operational (e.g., training), Physical (e.g., locks).  
  - **Types**: Preventive (block threats), Detective (identify breaches), Corrective (fix issues).  
  - **RTR Application**: Implement affordable firewalls (e.g., pfSense, free) and physical locks for SMBs.  
- **1.2 Fundamental Concepts**:  
  - CIA Triad (Confidentiality, Integrity, Availability), non-repudiation, AAA model (Authentication, Authorization, Accounting), zero-trust.  
  - **RTR Application**: Use zero-trust for client networks; train clients on password managers (e.g., Bitwarden, free).  
- **1.3 Change Management**:  
  - Document changes, assess risks, create backout plans.  
  - **RTR Application**: Standardize client IT updates using Trello for tracking (free tier).  
- **1.4 Cryptography**:  
  - PKI, encryption (file/database), hashing.  
  - **RTR Application**: Offer file encryption setups ($100-300/project) using VeraCrypt (free).  

**Tools**: pfSense, Bitwarden, VeraCrypt, Trello.  
**Skills to Practice**: Configure firewalls, set up password managers, document change processes.

### 2.0 Threats, Vulnerabilities, and Mitigations (22%)
**Core Knowledge**: Identify and mitigate threats to secure SMBs.  
**RTR Relevance**: Supports RTR’s cybersecurity audits and incident response services.  
- **2.1 Threat Actors**: Nation-state, hacktivists, insider threats; motivations (e.g., financial gain, disruption).  
  - **RTR Application**: Educate clients on phishing risks during workshops.  
- **2.2 Threat Vectors**: Phishing, SMS, unsecured Wi-Fi, supply chain risks.  
  - **RTR Application**: Scan client Wi-Fi with Wireshark (free) to identify vulnerabilities.  
- **2.3 Vulnerabilities**: Application bugs, misconfigurations, zero-days.  
  - **RTR Application**: Use OpenVAS (free) for vulnerability scans in audits.  
- **2.4 Malicious Activity**: Ransomware, DDoS, SQL injection.  
  - **RTR Application**: Simulate ransomware recovery in workshops using virtual machines.  
- **2.5 Mitigation**: Segmentation, patching, least privilege.  
  - **RTR Application**: Implement network segmentation for clients using VLANs on affordable routers (e.g., Ubiquiti EdgeRouter, ~$60).  

**Tools**: Wireshark, OpenVAS, VirtualBox (free).  
**Skills to Practice**: Run vulnerability scans, configure VLANs, simulate incident response.

### 3.0 Security Architecture (18%)
**Core Knowledge**: Design secure IT infrastructure for resilience.  
**RTR Relevance**: Informs RTR’s IT setup/enhancement services ($200-500/mo).  
- **3.1 Architecture Models**: Cloud, on-premises, IoT, microservices.  
  - **RTR Application**: Advise SMBs on hybrid cloud setups using Google Cloud free tier.  
- **3.2 Secure Infrastructure**: Device placement, VPNs, IDS/IPS.  
  - **RTR Application**: Set up OpenVPN (free) for secure client communications.  
- **3.3 Data Protection**: Encryption, tokenization, data classification.  
  - **RTR Application**: Classify client data (sensitive/public) during audits.  
- **3.4 Resilience and Recovery**: Backups, high availability, failover.  
  - **RTR Application**: Implement free backup solutions (e.g., Duplicati) for clients.  

**Tools**: OpenVPN, Google Cloud, Duplicati.  
**Skills to Practice**: Configure VPNs, design backup strategies, classify data.

### 4.0 Security Operations (22%)
**Core Knowledge**: Manage and monitor IT security operations.  
**RTR Relevance**: Supports RTR’s managed IT and automation services.  
- **4.1 Secure Baselines**: Harden devices and systems.  
  - **RTR Application**: Harden client servers using CIS benchmarks (free).  
- **4.2 Asset Management**: Track hardware/software, secure disposal.  
  - **RTR Application**: Use Snipe-IT (free) for client asset tracking.  
- **4.3 Vulnerability Management**: Scan, prioritize, remediate vulnerabilities.  
  - **RTR Application**: Schedule quarterly scans with OpenVAS.  
- **4.4 Monitoring**: SIEM, log analysis, alerts.  
  - **RTR Application**: Use Graylog (free) for client log monitoring.  
- **4.5 Security Enhancements**: Firewalls, IDS, email security (DMARC).  
  - **RTR Application**: Configure DMARC for client email using free DNS tools.  
- **4.6 Identity Management**: Multifactor authentication, least privilege.  
  - **RTR Application**: Set up 2FA with Authy (free) for clients.  
- **4.7 Automation**: Automate provisioning, ticketing.  
  - **RTR Application**: Automate client onboarding with Python scripts ($100-300/project).  
- **4.8 Incident Response**: Preparation, detection, recovery.  
  - **RTR Application**: Develop incident response plans for clients using NIST templates (free).  

**Tools**: CIS Benchmarks, Snipe-IT, Graylog, Authy, Python.  
**Skills to Practice**: Harden systems, automate tasks with Python, create incident response plans.

### 5.0 Security Program Management and Oversight (26%)
**Core Knowledge**: Establish governance, manage risks, ensure compliance.  
**RTR Relevance**: Enhances RTR’s consulting services and community advocacy.  
- **5.1 Governance**: Policies (AUP, incident response), standards.  
  - **RTR Application**: Draft client policies using free templates from SANS Institute.  
- **5.2 Risk Management**: Identify, assess, mitigate risks.  
  - **RTR Application**: Conduct risk assessments for clients using NIST 800-30 (free).  
- **5.3 Third-Party Risk**: Vendor assessments, SLAs.  
  - **RTR Application**: Evaluate client vendors during audits.  
- **5.4 Compliance**: GDPR/HIPAA basics, reporting.  
  - **RTR Application**: Ensure client compliance with free GDPR checklists.  
- **5.5 Audits**: Internal/external audits, penetration testing.  
  - **RTR Application**: Offer basic pen testing with Kali Linux (free).  
- **5.6 Security Awareness**: Phishing training, user education.  
  - **RTR Application**: Run phishing simulations in workshops using GoPhish (free).  

**Tools**: SANS templates, NIST 800-30, Kali Linux, GoPhish.  
**Skills to Practice**: Draft policies, conduct risk assessments, run phishing simulations.

## Practice Lab Setup (Affordable for RTR Clients/Workshop Attendees)
- **Hardware**: Used laptop ($100-200, local marketplaces), Raspberry Pi ($35) as a server, basic router (e.g., TP-Link, ~$30).  
- **Software**: VirtualBox, Kali Linux, pfSense, OpenVAS, Wireshark, Python (all free).  
- **Cloud**: Google Cloud free tier for testing cloud security.  
- **Setup Tips**:  
  - Use VirtualBox to simulate client networks.  
  - Configure Raspberry Pi as a firewall with pfSense.  
  - Practice packet analysis with Wireshark on local Wi-Fi.  

## Study Resources (Free/Low-Cost for Accessibility)
- **CompTIA Resources**: Free Security+ objectives PDF (download from CompTIA website).  
- **Online Courses**: IBM SkillsBuild (free cybersecurity courses), Professor Messer YouTube videos (free).  
- **Local Support**: ASBTDC (free business mentoring), Rock It! Lab (startup resources in Little Rock).  
- **Books**: “CompTIA Security+ Study Guide” (borrow from local libraries or buy used, ~$20).  
- **Practice Exams**: Free Security+ practice tests on ExamCompass.com.  

## Study Schedule (Tailored for Busy Entrepreneurs/Community Members)
- **Week 1-2**: Study Domain 1 (1 hr/day, 5 days/week); configure pfSense firewall.  
- **Week 3-4**: Domain 2; run OpenVAS scans in VirtualBox.  
- **Week 5-6**: Domain 3; set up OpenVPN and backup with Duplicati.  
- **Week 7-8**: Domain 4; write Python automation script for client onboarding.  
- **Week 9-10**: Domain 5; draft policy with SANS templates, run GoPhish simulation.  
- **Week 11-12**: Review all domains, take 2 practice exams/week (ExamCompass).  
- **RTR Tip**: Use Pomodoro (25-min study, 5-min break) to avoid burnout; join RTR’s quarterly workshops for hands-on practice.

## Key Metrics for Success
- **Pass Rate**: Aim for 80%+ on practice exams before scheduling the real exam.  
- **Workshop Impact**: Train 10-20 attendees per workshop; track certifications earned.  
- **Client Acquisition**: Use cheat sheet to attract 2-3 new SMB clients per workshop ($200-500/mo each).  

## Next Steps
- **For You**: Register for a free IBM SkillsBuild account; download CompTIA objectives PDF.  
- **For RTR**: Share cheat sheet on @RTRTechLR (X, Instagram) 3x/week; confirm for flyer design to promote workshops (image generation needed?).  
- **Community**: Partner with Little Rock’s Black Entrepreneurs group to distribute cheat sheet at networking events.

**RTR Branding**: “Securing Little Rock’s Future” – Empowering businesses and communities with knowledge and tools.  
**Contact**: info@rtrtechlr.com | @RTRTechLR | RTRTechLR.com (GitHub Pages)