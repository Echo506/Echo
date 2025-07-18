# 📋 **Note:**

These notes are a brief overview of the MITRE ATT&CK framework, highlighting key concepts and its utility in cybersecurity. For a comprehensive understanding, it's highly recommended to explore the official MITRE ATT&CK website and resources.

---

# **🛡️ MITRE ATT&CK Framework**

The **MITRE ATT&CK Framework** is an **open-source library** of various **attack paths** used by adversaries to infiltrate and operate within organizations. It serves as a crucial tool for **detecting and mitigating** these techniques.

* **Components of ATT&CK**: The acronym stands for **A**dversarial **T**actics, **T**echniques, and **C**ommon **K**nowledge, emphasizing observable methods.
* **Continuous Updates**: The framework is regularly updated to include new techniques and tactics, ensuring its relevance and effectiveness against evolving cyber threats.

---

## **Why MITRE ATT&CK? 🌟**

The MITRE ATT&CK framework is indispensable for modern cybersecurity operations due to several key advantages:

* **Standardization**: 🤝 It helps standardize cybersecurity terminology, facilitating effective communication among different teams (red, blue, and purple) and organizations, thereby minimizing miscommunication.
* **Global Repository**: 🌐 It acts as a global repository for the latest tools and techniques used by threat actors, enabling cybersecurity professionals to plan robust defenses and security measures.
* **Focus on TTPs**: 💡 The framework shifts the focus from traditional Indicators of Compromise (IOCs) to **Tactics, Techniques, and Procedures (TTPs)**. TTPs are more challenging for attackers to alter, making them more reliable for tracking potential threats.

---

## **Overview of the Framework: 🗺️**

The MITRE ATT&CK framework is structured to provide a comprehensive view of adversary behavior:

* **Three Main Pillars**: It is organized around three primary components: **ATT&CK matrices**, **ATT&CK tactics**, and **ATT&CK techniques**.
* **ATT&CK Matrices**: These include specialized categories such as **Enterprise**, **Mobile**, and **Industrial Control Systems (ICS)**, each focusing on different types of attack targets.
* **Tactics and Techniques**: **Tactics** represent the "why" behind an attacker's actions (their high-level objectives), while **techniques** detail the "how" of achieving those objectives. Techniques can be further broken down into **sub-techniques** for more granular detail.
* **Data Sources**: 📊 These are various log sources (e.g., Active Directory, anti-malware tools, firewalls) used to prioritize monitoring activities and identify signs of adversary activity.
* **Groups**: 👥 Information about different hacker groups and APTs, detailing their unique tactics and techniques, each tagged with a unique ID.
* **Software**: 💻 A collection of tools and solutions commonly employed by adversaries.
* **Campaigns**: 🗓️ Details on active and historic cyber attack campaigns observed around the world.

---

<details>
  <summary><h2>**Understanding the Phases of Attack ➡️**</h2></summary>

The MITRE ATT&CK framework categorizes adversary behavior into several tactical phases, reflecting the typical stages of a cyber attack:

### **1. 🔍 Reconnaissance**

* **Reconnaissance Tactic (TA0043)**: This initial phase involves **active or passive information gathering** to learn more about the target before launching an attack.
* **Common Techniques**:
    * **Active Scanning (T1595)**: Involves IP-based and vulnerability scans to identify potential entry points into the target infrastructure.
    * **Searching Open Technical Databases (T1596)**: Utilizes sources like WHOIS records, DNS registries, and SSL certificates to gather technical information about the target network.
    * **Searching Public Websites (T1593)**: Involves collecting information from social media, public code repositories, search engines, and other publicly available sources.

### **2. 🏗️ Resource Development**

* **Resource Development Tactic (TA0042)**: This phase involves **setting up support infrastructure** needed for later stages of a cyberattack.
* **Common Techniques**:
    * **Acquire Access (T1650)**: Obtaining access to the target system or infrastructure, which can be built, borrowed, bought, leased, or compromised.
    * **Develop Capabilities (T1583)**: Setting up IT infrastructure required for attacks, such as bots for denial-of-service or command-and-control centers for malware.
    * **Establish Accounts (T1585)**: Creating fraudulent identities, webpages, or online profiles to facilitate social engineering attacks.

### **3. 🚪 Initial Access**

* **Initial Access Tactic**: Techniques used by attackers to gain **preliminary access** to the target environment. This access can be either temporary or persistent.
* **Common Techniques**:
    * **Drive-by Compromise (T1189)**: Compromised websites with malicious code designed to steal authentication credentials from a victim's browser.
    * **Exploitation of Public-Facing Infrastructure (T1190)**: Exploiting vulnerabilities in publicly exposed assets like websites and servers to gain initial access.
    * **Exploitation of Public-Facing Remote-Access Services (T1133)**: Compromising remote-access technologies like SSH, RDP, and VPNs to access the target network.

### **4. ⚙️ Execution**

* **Execution Tactic**: Involves techniques used by attackers to **run malicious code or scripts** in the target environment.
* **Techniques and Sub-Techniques**: There are 14 techniques and 22 sub-techniques under this tactic, including:
    * **Cloud Administration Tools (T1651)**: Compromising cloud administration tools like AWS Systems Manager and Azure AD to execute scripts.
    * **Command and Scripting Interpreter (T1059)**: Using compilers and interpreters installed on the compromised environment to run scripts in languages like Python, JavaScript, and PowerShell.
    * **Client-Side Exploitation (T1203)**: Exploiting vulnerabilities in client-side software such as web browsers and FTP clients to execute scripts.

### **5. ⏳ Persistence**

* **Persistence Tactic**: Ensures attackers **maintain access** to a compromised system despite interruptions like system reboots or password changes.
* **Common Techniques**:
    * **Create Account (T1136)**: Creating additional user accounts with high privileges to maintain access independently of the compromised account.
    * **Account Manipulation (T1098)**: Manipulating account privileges, such as changing passwords or adding trusted devices, to maintain access.
    * **Boot or Logon Autostart Execution (T1547)**: Modifying system boot processes or auto-start settings to run attacker-controlled scripts upon system startup.

### **6. ⏫ Privilege Escalation**

* **Privilege Escalation Tactic**: Allows attackers to **gain higher privileges** than they currently possess, crucial for running malicious code, bypassing security controls, and maintaining persistent access.
* **Common Techniques**:
    * **Exploitation for Privilege Escalation (T1068)**: Exploiting system or OS-level vulnerabilities, such as Windows' Sticky Key vulnerabilities and Linux kernel privilege escalation.
    * **Valid Accounts (T1078)**: Using compromised credentials to access pre-existing privileged accounts and bypass access controls.
    * **Domain Policy Modification (T1484)**: Modifying configuration settings of a domain controller to escalate privileges in a domain-joined environment.

### **7. 👻 Defense Evasion**

* **Defense Evasion Tactic**: Consists of **42 techniques** aimed at **bypassing or fooling security controls** in a target environment.
* **Common Techniques**:
    * Hiding malicious code under OS processes like `RunDLL` or `System32`.
    * Bypassing security tools such as antivirus, EDR solutions, and monitoring controls.
    * Techniques include masquerading system tasks, modifying domain policies, and deleting log files or command traces.

### **8. ➡️ Lateral Movement**

* **Lateral Movement Tactic**: Techniques that allow an attacker to **move from one system or network to another** within the compromised environment.
* **Techniques and Sub-Techniques**: There are 9 techniques and 13 sub-techniques under lateral movement.

### **9. 📥 Collection**

* **Collection Tactic**: Techniques used to **accumulate critical information** from the target device, such as keystroke capture, audio-video capture, and copying data from databases.
* **Techniques and Sub-Techniques**: There are 17 techniques and 17 sub-techniques under collection.

### **10. 📞 Command and Control (C2)**

* **Command and Control Tactic**: Techniques that allow hackers to **communicate with compromised hosts** to achieve persistence, collection, and other goals.
* **Techniques and Sub-Techniques**: There are 16 techniques and 23 sub-techniques under command and control.
</details>

---

<details>
  <summary><h2>**Integrating MITRE ATT&CK 🧩**</h2></summary>

### **Integration in Security Operations**

* The ATT&CK framework is a valuable resource for **planning and executing various security operations**, such as security monitoring and hardening controls.
* **Utilizing Data Sources**: Use the **data sources section** to identify different log sources (e.g., active directory, application logs, SSL certificates) for detecting ATT&CK techniques.
* **Mitigation and Software Sections**: The **mitigation section** provides controls to prevent ATT&CK techniques, while the **software section** helps identify malicious tools and hacker groups to configure preventive or detective tools.

### **Using ATT&CK to Equip Threat Intelligence**

* **Open Source Intelligence**: MITRE collects **open-source intelligence globally** and makes it available through the ATT&CK framework, providing a repository of adversary tactics, techniques, and attacker groups.
* **Cataloging Hacker Groups**: ATT&CK catalogs various attacker and APT groups, detailing the techniques and sub-techniques they use, as well as the software involved in their activities.
* **Tracking Cyber Attack Campaigns**: The framework helps keep track of **cyber attack campaigns** observed worldwide, making it a valuable resource for running a threat intelligence program.

### **Integrating MITRE ATT&CK with Security Tools**

* **Tool Selection**: The ATT&CK framework helps in **deciding which security tools to purchase** by mapping out which techniques or sub-techniques are covered by these tools.
* **Planning Security Operations**: Use the framework to **plan your security operations and layer defense models** effectively.
* **Identifying New Tools**: The framework aids in **identifying new tools needed** for your organization by highlighting gaps in current tool coverage.

### **Best Practices for Using the Framework**

To maximize the benefits of the MITRE ATT&CK framework:

* **Identify Relevant Threat Actors**: Determine specific threat actors or groups relevant to your organization or industry to prioritize your defense strategies.
* **Map Techniques to Your Environment**: Identify which ATT&CK techniques are applicable to your network, system, or assets to plan your defense and identify potential vulnerabilities.
* **Regular Assessments**: Perform regular assessments and simulations, such as red teaming or penetration testing, to test your defenses and validate your security controls.
* **Incorporate into Security Operations**: Use the framework to enhance threat-hunting, incident response, and detection capabilities by developing playbooks and use cases based on ATT&CK.
</details>

---

<details>
  <summary><h2>**ATT&CK Navigator: 🧭**</h2></summary>

The **ATT&CK Navigator** is a powerful visual tool for interacting with the framework:

* [MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/)
* **Visualization Tool**: The ATT&CK Navigator provides a **visual representation** of the ATT&CK framework, which helps in mapping out and understanding cyber attack paths.
* **Creating Layers**: You can **create new layers** from scratch or import existing ones, and customize them with metadata, colors, and other options to highlight specific aspects.
* **Feature Highlights**: The tool offers features like selection behavior, search, unselect options, and the ability to download layers in various formats (JSON, Excel, image).
</details>
```
