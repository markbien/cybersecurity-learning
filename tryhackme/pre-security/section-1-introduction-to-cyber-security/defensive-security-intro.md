# 🛡️ Pre-Security - Defensive Security Intro

## 🧠 What I learned

### Task 1 - Introduction to Defensive Security
- This role is mainly focused on protecting the company from unauthorized access and attacks from "red team"
- Prevents intrusion from occurring
- Detect intrusions when they occur and respond accordingly
- a.k.a. "Blue team"
- Some of the tasks:
  - Train users about cybersecurity to avoid attacks
  - Know the systems to manage and protect
  - Ensure all devices are updated and patched to fix vulnerabilities
  - Setup security devices such as [firewall](#firewall-definition) and intrusion prevention systems or [IPS](#ips)
  - setup logging and monitoring devices

- Some of the roles:
  - Security Operations Center (SOC)
  - Threat Intelligence
  - Digital Forensics & Incident Response (DFIR)
  - Malware Analysis


### Task 2 - Areas of Defensive Security
- Security Operations Center (SOC)
  - a team of cybersec professionals that monitors network and sytems to detect unauthorized access or attacks:
    - fix vulnerabilities
    - set of rules to protect the network and systems
    - review unauthorized activity, detect, and block an event before further damage is done
    - detect intrusions ASAP to prevent further damage

- Threat Intelligence
  - intelligence a.k.a. information you gather about actual and potential enemies
  - threat a.k.a any action that can disrupt or badly affect a system
  - threat intelligence collects info to help company protect against potential adversaries
  - be able to become "threat-informed defence"
  - different companies have different adversaries
  - Intelligence needs data, and data has to be collected, processed, and analyzed
  - can be collected from local sources such as network logs, public sources such as forums
  - data processing arranges it to format suitable for analysis
  - analysis seeks to find more info about attackers and their motives

- Digital Forensices and Incident Response (DFIR)
  - Digital Forensics
    - application of science to investigate crimes and establish facts in digital systems
    - focuses on:
      - file system
      - system memory
      - system logs
      - network logs
  - Incident Response
    - incident refers to data breach or cyber attacks
    - can be less critical such as misconfig, intrusion attempt, or policy violation
    - 4 Phases of IR:
      1. Preparation - requires team to be trained and ready to handle incidents. Prevent incidents from happening in the first place
      2. Detection and Analysis - detect and analyze incident to learn about severity
      3. Containment, Eradication, and Recovery - stop incidents, eliminate, and recover affected systems
      4. Post-Incident Activity - a report is produced and lesson is shared to prevent similar future incidents
  - Malware Analysis
    - virus is a piece of code that attaches itself to a program. designed to spread from one computer to another and works by altering, overwriting, and deleting files once a device is infected
    - Trojan Horse is a program that shows a desirable function but hides malicious function underneath
    - Ransoware is a malicious program that encrypts a file and an attacker offers encryption password if the user is willing to pay a ransom
    - aims:
      1. Static Analysis - inspect a malicious program without running it
      2. Dynamic Analysis - run a malware in a controlled environment and monitor activities

### Task 3 - Practical Example of Defensive Security
- Accessed a simulation of SIEM where I saw informatino about alerts
- Incluldes:
  - Date
  - Message / Activity
  - Found 1 unauthorized activity and used it to enter ip address and get the flag


## 📚 Keyword Definitions
### firewall - security tool, hardware or software used to filter network traffic by stopping unauthorized incoming or outgoing traffic
<a name="firewall"></a>

### IPS - a device or app that detects and stops intrusions attempts proactively
<a name="ips"></a>