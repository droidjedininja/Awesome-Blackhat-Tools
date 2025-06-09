# 🔴 Red Teaming Tools

> This document lists all tools categorized under **Red Teaming** from various Black Hat Arsenal events (Asia, USA, Europe, etc.) across all years.

Red Teaming involves offensive tactics, adversary simulations, lateral movement, social engineering, privilege escalation, and post-exploitation. The tools listed here assist in such activities.



## 🔧 Tools List

-  ### 📅 2025

    - <details><summary><strong>Automating Red Team Operations in Windows AD with Local LLM and Multi AI Agents</strong></summary>

      📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

      🔗 [GitHub](https://github.com/daqcri/deeper-lite/blob/master/python/BenchmarkDatasets/DBLP_ACM/ACM.csv)

      📝 **Description:** Modern Red Team assessments in Windows Active Directory (AD) environments often involve navigating a vast array of machines, accounts,          making them highly resource-intensive. To streamline these engagements, I developed a prototype automated penetration testing tool that leverages local            Large Language Models (LLMs) and specialized AI Agents. Because AD environments often contain large amounts of confidential data, this solution can operate        entirely within a closed environment, mitigating the risk of data leakage. I verified that the system runs effectively on a single PC.

      A fundamental challenge with local LLMs is that they often lack sufficient domain-specific knowledge, particularly with regard to attacker tools and               methodologies. I address this limitation by restricting the set of utilized tools (e.g., Mimikatz, Psexec, PowerView) and designing specialized Agents for         each. I also enhance the models' reasoning with Retrieval-Augmented Generation (RAG) pipelines that focus on typical AD attack paths. Each Agent is based on       the ReAct model and logs its thought process and executed commands to visualize the flow of reasoning.

      Beyond the immediate goal of reducing the effort required for Red Team operations, this research also examines a future threat vector. I anticipate that           adversaries will soon embed local LLMs into malware, enabling offline attacks on isolated machines—such as web-isolated hosts or local networks. These             attacks do not generate network traffic, thereby evading detection by security appliances that monitor outbound traffic. To evaluate the potential efficacy        of local AI-driven automation—given that most Windows devices are equipped only with a CPU—this tool will be tested using a model that runs on the CPU.

     </details>

   - <details><summary><strong>BOAZ: Development of a Multilayered Evasion Tool and Methodology</strong></summary>

     📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)

     🔗 [GitHub](https://github.com/ICTMCG/Awesome-Machine-Generated-Text/blob/main/README.md)

      📝 **Description:** BOAZ (Bypass, Obfuscate, Adapt, Zero-Trust) evasion was inspired by the concept of multi-layered approach which is the evasive version         of defence-in-depth first proposed by at BH USA14 [1]. BOAZ was developed to provide greater control over combinations of evasion methods, enabling more           granular evaluations against antivirus and EDR. It is designed to bypass both before and during execution detections that span signature, heuristic and            behavioural detection techniques [2].

      BOAZ supports both x86/x64 binary (PE) or raw payload as input and output EXE or DLL. It has been tested on separated Window-11 Enterprise, Windows-10 and         windows Server 2022 VMs (version: 22H2, 22621.1992) with 14 Desktop AVs and 7 EDRs installed include Windows Defender, Norton, BitDefender, Sophos and ESET.       The design of BOAZ evasion is modular, so users can add their own toolset or techniques to the framework. One advantage of this approach is that if a              specific technique's signature become known to antivirus, researchers can easily adjust the technique to verify it and either improve or target a new              technique to that detection. This process is described as a query-modify-query attack process, where the attacker can improve based on the feedback from           black-box engines until their sample is fully undetectable (FUD) [3].

      BOAZ is written in C++ and C and uses Python3 as the main linker to integrate all modules. There have been significant improvements implemented since its          inception. The new features of the BOAZ evasion tool, set to be released at BH Asia 2025, include two novel process injection primitives, along with newly         implemented loaders and behavioural evasion techniques. There will be a major update to the BH USA 2025 version, including some new anti-forensic techniques       and more new process injection threadless execution primitives.

      </details>

   - <details><summary><strong>Crucible C2: Offensive Security Reforged</strong></summary>

      📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

      🔗 **GitHub:** Not Available  
      📝 **Description:** Crucible is an extensible, multi-user, cross-platform framework designed for post-exploitation, command and control operations,                 penetration testing, and red teaming.

       It consists of a per-operator client application, a shared teamserver, and supports language-agnostic implants and plugins.

       With this release of Crucible, modern extensibility is achieved through in-memory .NET plugins or gRPC-based plugins, enabling remote communication with           external applications regardless of language, allowing extensibility that fits both the operator's skill set and needs.

        </details>

   - <details><summary><strong>DeadMatter: Offset Independent Credential Extraction Tool</strong></summary>

     📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

     🔗 **GitHub:** Not Available  
      📝 **Description:** DeadMatter is a specialized tool written in C#, designed to extract sensitive information such as password hashes of active logon              sessions, from memory dumps. It employs carving techniques to retrieve credentials from various file types such as process or full memory dumps, either in          raw or minidump format, decompressed hibernation files, virtual machine memory files, or other types of files that may contain logon credentials.

      This tool is particularly useful for penetration testers, red teamers, and forensic investigators, as it facilitates the analysis of system security               vulnerabilities and aids in digital forensic investigations. DeadMatter can be very useful to pentesters and red teamers during their engagements, since           they often have to deal with EDR and AV software detecting and/or blocking their attempts to dump the LSASS process memory in the minidump format. The             alternative of dumping and exfiltrating a full memory dump is often not an option. As a result, DeadMatter was created to fill the gap and allow the               offensive team to parse the memory dump files directly on the victim machine, in order to extract NTLM hashes on the spot.

</details>

<details><summary><strong>EntraGoat - A Deliberately Vulnerable Entra ID Environment</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** Not Available  
📝 **Description:** EntraGoat is a deliberately vulnerable environment designed to simulate real-world security misconfigurations and attack scenarios in Microsoft Entra ID (formerly Azure Active Directory). Security professionals, researchers, and red teamers can leverage EntraGoat to gain hands-on experience identifying and exploiting identity and access management (IAM) vulnerabilities, privilege escalation paths, and other security flaws specific to cloud-based Entra ID environments.
EntraGoat is tailored specifically to help security practitioners understand and mitigate the risks associated with cloud identity infrastructures. The project provides a CTF-style learning experience, covering a range of misconfigurations, insecure policies, token abuses, and attack paths commonly exploited in real-world Entra ID breaches.
By using EntraGoat, security teams can enhance their skills in Entra ID security, validate detection and response capabilities, and develop effective hardening strategies.

</details>

<details><summary><strong>From Recon to Pwn: MSSQL Exploitation with MSSqlPwner</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** Not Available  
📝 **Description:** MSSqlPwner is a sophisticated penetration testing arsenal specifically engineered to dominate Microsoft SQL Server environments. Leveraging the extensive capabilities of the Impacket toolkit, MSSqlPwner arms penetration testers with a powerful suite of exploitation techniques, including authentication attacks using Kerberos tickets, NTLM hashes, and clear-text credentials. This versatile tool excels at advanced maneuvers such as NTLM relay attacks, Kerberos and NTLM password bruteforcing, and even direct password extraction via LDAP integration—transforming standard SQL servers into strategic entry points for escalating privileges and lateral network infiltration.

</details>

<details><summary><strong>Glato: GitLab Attack Toolkit</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** Not Available  
📝 **Description:** CI/CD pipelines are a too often overlooked aspect of the attack surface for many large organizations. Recent tooling has enabled engineers, researchers, and attackers to search GitHub for CI/CD vulnerabilities, but other DevOps platforms, like GitLab, have been left underserved.

Glato (GitLab Attack Toolkit) is an enumeration and attack framework that empowers both blue and red teamers in identifying and exploiting vulnerabilities within GitLab instances.
Glato works across all GitLab environments, including GitLab CE, EE, and GitLab Cloud. The tool is field-tested, having identified attack paths to GitLab Admin, Domain Admin, and Cloud Admin in multiple engagements with real Fortune 500 organizations.

GitLab's CI/CD ecosystem can contain configuration vulnerabilities that expose organizations to token privilege escalation, sensitive data exposure, and arbitrary code execution on self-hosted runners. Glato's enumeration module leverages a personal access token or session cookies to systematically map all accessible repositories, groups, and instance-level resources. Through recursive pipeline workflow analysis, it identifies misconfigurations and vulnerable CI/CD pipelines that create attack paths within and beyond the GitLab environment.

Security practitioners can deploy Glato's attack module to securely exploit these misconfigurations with features including encrypted variable exfiltration via Poisoned Pipeline Execution (PPE) attacks, secrets dumping, and self-hosted runner compromise. The tool's architecture ensures auditability and operational security through selective targeting and clean exfiltration methods.

Glato has already been used in secure assessments and Red Team engagements to escalate privileges and compromise entire cloud environments.


Key Features:
1. Token/Cookie Authentication Analysis: Evaluates permissions and scope of GitLab tokens or session cookies
2. Comprehensive Enumeration: Discovers accessible projects, groups, and resources with their permission levels
3. Branch Protection Analysis: Identifies misconfigurations that could lead to code execution
4. Secret Discovery: Enumerates secrets from multiple sources, including CI/CD variables
5. Runner Enumeration: Identifies potentially accessible self-hosted runners
6. Poisoned Pipeline Execution: Enables secure CI/CD pipeline exploitation with encrypted secrets exfiltration
7. Quality-of-Life Features: Proxy support, SSL verification control, request throttling, cookie-based authentication for SSO environments, and detailed reporting options

Glato provides security professionals with a systematic approach to evaluate GitLab environments and identify CI/CD pipeline risks before malicious actors can exploit them.

</details>

<details><summary><strong>Introducing RAVEN - Discovering and Analyzing CI/CD Vulnerabilities in Scale</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** Not Available  
📝 **Description:** As the adoption of CI/CD practices continues to grow, securing these pipelines has become increasingly important. However, identifying vulnerabilities in CI/CD pipelines can be daunting, especially at scale. In this talk, we present our tooling, which we have released as open-source software, enabling us to uncover hundreds of vulnerabilities in the CI/CD pipelines of popular open-source projects.

RAVEN (Risk Analysis and Vulnerability Enumeration for CI/CD) is a powerful security tool designed to perform massive scans for GitHub Actions CI workflows and digest the discovered data into a Neo4j database. With RAVEN, we were able to identify and address potential security vulnerabilities in some of the most popular repositories hosted on GitHub, including FreeCodeCamp, Fluent UI by Microsoft, Bazel by Google, and much more.
This tool provides a reliable and scalable solution for security analysis, enabling users to query the database and gain insights about their codebase's security posture.

</details>

<details><summary><strong>Java Chains: Make Java Vulnerability Exploit brilliant again</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** Not Available  
📝 **Description:** This tool focuses on the Java security domain, dedicated to providing comprehensive Java vulnerability payload generation and exploitation capabilities. It supports practical utilization in various real-world scenarios, covering payload generation for common vulnerabilities like Java deserialization and Hessian deserialization, as well as exploitation of vulnerabilities such as JNDI injection and RMI deserialization.

</details>

<details><summary><strong>Metasploit's Latest Attack Capability and Workflow Improvements</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  
🔗 **GitHub:** Not Available  
📝 **Description:** Metasploit continues to expand support for Active Directory Certificate Services (AD CS) attacks, as well as its protocol relaying capability and attack workflows for evergreen vulnerabilities. This year, we added support for SMB-to-LDAP relaying and SMB-to-HTTP relaying, as well as support to identify and exploit a number of AD CS flaws (i.e., ESC vulnerabilities). We've also added the new "PoolParty" process injection capability to Windows Meterpreter sessions, along with support for System Center Configuration Manager (SCCM) attack workflows.


This demo will focus on obtaining an LDAP session via SMB relaying, which can then be used to identify ESC vulnerabilities through Metasploit's expanded ldap_vulnerable_cert_finder module. Using the results from the vulnerable cert finder module, we will demonstrate how to detect and exploit ESC15 (the newest ESC vulnerable certificate template flaw) in order to obtain a certificate that can be used to open a Windows Meterpreter session. While opening the Meterpreter session we will demonstrate using Sysmon how the Windows Meterpreter no longer makes calls to CreateRemoteThread and instead uses the PoolParty injection technique to more effectively inject into the target process.

Going back to our LDAP session, we will run a query to identify SCCM servers in the target Active Directory environment. Once identified, we will demonstrate Metasploit's new SCCM attack workflow, which leverages new SMB-to-HTTP relaying capabilities. Using Metasploit's SMB-to-HTTP relay server, we will relay an NTLM authentication attempt for a newly created computer account to the SCCM HTTP authentication server. After successfully authenticating, we will retrieve Network Access Account (NAA) credentials from the SCCM server, as these are often found in domain environments with higher privileges than they require making them a prime target for lateral movement.

</details>

<details><summary><strong>MORF – Mobile Reconnaissance Framework</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** Not Available  
📝 **Description:** MORF is a versatile, lightweight, and platform-independent offensive mobile security tool that aids security professionals and developers in detecting sensitive information within mobile applications. Often referred to as a "Swiss army knife" for mobile app security, MORF utilizes heuristics-based methods to quickly discover keys, secrets, and other crucial data. Its extensible plugin framework accommodates custom rules and integrations, making it adaptable to specific projects or organizational needs for both Android and iOS environments.

</details>

<details><summary><strong>OffensiveSwift</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  
🔗 **GitHub:** Not Available  
📝 **Description:** Red teamers often rely on command-line tools for macOS testing, making them highly detectable by endpoint security solutions. OffensiveSwift is a modern offensive framework built entirely in Swift, offering a native approach to macOS adversary emulation. It leverages Swift's direct access to macOS APIs—without invoking traditional shell commands—to minimize observable traces and lower its detection footprint.

Highlights:

- Standalone Binary: Compiles directly into a standalone binary with no external dependencies.
- Reduced Detections: Uses macOS APIs for a more stealthy and efficient operation.
- Flexible TTP Chaining: Provides programmatic interfaces that seamlessly chain TTPs into complex adversary simulations.
- Modular Design: Supports both individual technique testing and the creation of full emulation campaigns.

</details>

<details><summary><strong>Penelope shell handler</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** [Penelope shell handler](https://gist.github.com/FabioXimenes/17b544471ba4790fcdd289fc190b3467)  
📝 **Description:** Penelope is a shell handler designed to be easy to use and intended to replace netcat when exploiting RCE vulnerabilities. It is compatible with Linux and macOS and requires Python 3.6 or higher. It is a standalone script that does not require any installation or external dependencies, and it is intended to remain this way.

Among the main features are:

* Auto-upgrade shells to PTY (realtime resize included)
* Logging interaction with the targets
* Download files/folders from targets
* Upload local/remote files/folders to targets
* Run scripts on targets and get output on a local file in real time.
* Port Forwarding
* Spawn shells on multiple tabs and/or hosts
* Maintain X amount of active shells per host no matter what
* Multiple sessions
* Multiple listeners
* Can be imported by python3 exploits and get shell on the same terminal

Penelope can work in conjunction with metasploit exploits by disabling the default handler with `set DisablePayloadHandler True`

Currently only Unix shells are fully supported. There is only basic support for Windows shells (netcat-like interaction + logging) and the rest of the features are under way.

</details>

<details><summary><strong>RedInfraCraft : Automate Complex Red Team Infra</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** Not Available  
📝 **Description:** RedInfraCraft is a powerful FOSS solution for automating the deployment of powerful red team infrastructures. It streamlines the setup and management of :

- Individual Red Team Components (C2, Payload, Redirector Server etc.)
- On-premise / Cloud services re-director support
- Complete Red Team Infrastructure (Redirector Load Balancer C2, Payload server, phishing server etc)
- Phishing Operations
- Infrastructure deployment support in AWS, Azure & GCP Cloud including multi-cloud support.

Dilute your time to setup Red Team Infrastructure in 5 minutes with RedInfraCraft

</details>

<details><summary><strong>ROP ROCKET: Advanced Framework for Return-Oriented Programming</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 [GitHub](https://github.com/Bw3ll/ROP_ROCKET)

📝 **Description:** ROP ROCKET is a groundbreaking, next-generation tool for Return-Oriented Programming (ROP), boasting unparalleled capabilities. This tool introduces several innovative techniques, including a novel approach to invoking Heaven's Gate via ROP, which facilitates the transition from x86 to x64 architecture, and invoking Windows syscalls via ROP to evade Data Execution Prevention (DEP), eliminating the need for less stealthy Windows API functions.

The focal point of this tool is automatic ROP chain generation—constructing complete ROP exploits. Moreover, with this tool, we pioneer several new ROP techniques, including both x86 and x64 Heaven's Gate and using Windows syscalls to bypass DEP. To overcome DEP, we automate chain generation for Windows syscalls NtAllocateVirtualMemory and NtProtectVirtualMemory. In addition, ROP ROCKET can avoid the need to bypass DEP by chaining multiple APIs together to achieve shellcode-like functionality.

For Black Hat Arsenal 2025, we will unveil support for building ROP chains for many new WinAPIs: WinExec, DeleteFileA, CreateToolhelp32Snapshot, URLDownloadToFileA, OpenProcess, Process32First, Process32Next, RegSetKeyValueA, RegCreateKeyA, WriteProcessMemory, HeapCreate, OpenSCManagerA, CreateServiceA, ShellExecuteA, CreateRemoteThread, VirtualAllocEx, TerminateProcess, and CreateProcessA. All will be available via automatic ROP chain construction using patterns with PUSHAD or a combination of PUSHAD coupled with mov dereferences, or the sniper approach.

One of the features of ROP ROCKET is the sheer diversity of possibilities in creating these chains, allowing unique and unusual combinations that traditionally might not be achievable by ROP chain automation. The tool uses extensive emulation to evaluate the fitness of individual ROP gadgets, allowing unusual or longer ROP gadgets to be used. It also builds, emulates, and debugs parts of some ROP chains internally to solve certain problems, allowing for ROP chains to be built with the mov dereference or sniper approach, rather than relying simply on the PUSHAD approach. Distances to certain function parameters can also be dynamically calculated and readjusted with emulation.

Sometimes a ROP chain is feasible only if a ROP gadget's address is free of bad bytes. With ROP ROCKET, we provide a way to obfuscate gadgets, allowing the gadget address to be pushed onto the stack, decoded, and executed at runtime.

ROP ROCKET is built for performance, utilizing multiprocessing to harness a dozen or more cores. It also stores discovered gadgets from previously examined binaries, giving persistence across sessions. With all possible ROP gadgets—our raw ingredients—identified, ROP chains can be formed in seconds.

While ROP can be a complex topic, ROP ROCKET provides powerful capabilities to users. New for Black Hat Arsenal 2025, the tool will support over 100 patterns for different WinAPIs or syscalls, far exceeding the capabilities of other ROP generation tools.

</details>

<details><summary><strong>SAMLSmith</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** Not Available  
📝 **Description:** SAMLSmith is the go-to tool for penetrating SAML applications with response forging. An evolution of the original tooling developed for proof-of-concept of SAML response forging in Entra ID, SAMLSmith takes further research around SAML response forging and combines it into a tool crafted for offensive scenarios.

While far from new, enterprises continue to not prioritize the security of how SaaS applications integrate or understand best practices for securing them. With many factors at play, SAML response forging can range from extremely difficult to near impossible for a SOC to detect.

SAMLSmith has a lot of tricks up its sleeve, including:
- Multiple identity provider response forging
- AD FS specific response forging mode
- SAML request processing
- InResponseTo support

SAMLSmith can be used in several response forging scenarios where the private key material can be obtained. In demonstration of use, we'll explore using SAMLSmith for performing a Golden SAML attack against AD FS. Further, we'll demonstrate the use of SAMLSmith that ties into new research around response forging, penetrating certain types of SaaS applications with even more stealth.

Using SAMLSmith requires a certain level of knowledge about the target environment, much of which can be gained with other commonly known and used tools that perform reconnaissance against the targeted identity provider.

</details>

<details><summary><strong>SCCMHunter</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 [GitHub](https://github.com/garrettfoster13/sccmhunter/wiki)

📝 **Description:** SCCMHunter is a post-exploitation tool built to streamline identifying, profiling, and attacking SCCM related assets in an Active Directory domain.

In this update, SCCMHunter has received additions to the recon module for site system profiling, the admin module has been extended for more post-exploitation commands, and a new relay module has been built for credential relaying.

The presentation will include a walkthrough of the tool and it's various modules and a demonstrations of how to use the modules for SCCM hierarchy takeover

</details>

<details><summary><strong>Sickle - Payload Development Framework</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 [GitHub](https://github.com/wetw0rk/Sickle)

📝 **Description:** This presentation explores Sickle, a modular and extensible payload development framework designed for offensive security professionals and red teamers. Sickle enhances exploit development by providing a structured approach to crafting highly sophisticated payloads for the modern landscape.

Attendees will gain insight into Sickle's dynamic payload generation and multi-stage execution capabilities. The talk will cover key features such as customizable shellcode, and integration with existing exploitation frameworks.

A live demonstration will showcase how Sickle can be used to generate and deploy payloads tailored to specific target environments, emphasizing its adaptability in real-world engagements.

By the end of the session, participants will understand how to leverage Sickle to craft advanced payloads while adhering to ethical and legal considerations in penetration testing and red teaming.

</details>

<details><summary><strong>Tengu Marauder: Combining Robotics and Cybersecurity</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** Not Available  
📝 **Description:** The Tengu Marauder, derived from a previous security drone project, is a portable wheeled robot equipped with an ESP32 Marauder, currently in its testing phase. Designed for simplicity and efficiency, the Tengu Marauder serves as an alternative and interactive tool for WiFi network security testing. Its capabilities include WiFi scanning, deauthentication attacks, packet sniffing, and other wireless security tests. The compact design ensures ease of construction and maintenance using readily available parts and straightforward code integration. Essentially an advanced RC robot, the Tengu Marauder operates headless via XBee, providing a fun and engaging platform for testing the security of network-controlled devices over WiFi, such as IoT smart home devices and smaller WiFi-controlled drones like the Ryze Tello. This project would not have been possible without the support of local Philadelphia security organizations and the overall security community.

</details>

<details><summary><strong>Utilizing Native Messaging API for Covert Command and Control (C3)</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** [Utilizing Native Messaging API for Covert Command and Control (C3)](https://github.com/efchatz/Covert-C2)  
📝 **Description:** Traditional Command and Control (C2) frameworks frequently encounter obstacles in avoiding detection, maintaining persistence, and ensuring resilience against modern security measures. This research introduces Covert C2, an advanced Covert Command and Control (C3) system engineered to enhance operational security while minimizing detection risks through widely used persistence strategies. Covert C2 employs a decentralized infrastructure, enabling compromised machines to autonomously establish communication with the C2 server, thereby ensuring sustained covert operations. Its adaptable design supports various post-exploitation and lateral movement methods, optimizing functionality across different environments. By utilizing the Native Messaging API alongside lightweight evasion techniques, Covert C2 agents demonstrate an exceptionally zero detection rate against top-tier Endpoint Detection and Response (EDR) solutions. A proof-of-concept implementation confirms Covert C2's effectiveness in real-world adversarial scenarios, particularly in executing code for privilege escalation and lateral movement. Our assessment underscores that merging decentralized communication with innovative evasion methods significantly boosts stealth, efficiency, and operational resilience. Furthermore, this study explores Covert C2's post-exploitation capabilities, assesses defensive strategies, and provides practical recommendations for enhancing cybersecurity defenses.

</details>

<details><summary><strong>Warhead: Stealthy Payload Execution via Atom Tables</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** [Warhead: Stealthy Payload Execution via Atom Tables](https://gist.github.com/Lysak/a0ca30a3e6732d39199b27c170a8cd28)  
📝 **Description:** Warhead is an offensive security tool that leverages Windows Atom Tables to store, retrieve, and execute payloads in a stealthy manner. This technique enables adversaries to place a payload in the Atom Table, use a legitimate process to extract it, and execute it in memory—bypassing traditional detection mechanisms. The first version of Warhead, to be released at Black Hat Arsenal 2025, provides security researchers and red teamers with a novel approach to payload delivery and execution that evades modern security defenses.

</details>

<details><summary><strong>wish: An AI-Powered Natural Language Shell for Penetration Testing</strong></summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2025-blue)](https://github.com/UCYBERS/Awesome-BlackHat-Tools)  

🔗 **GitHub:** [wish: An AI-Powered Natural Language Shell for Penetration Testing](https://github.com/rtholmes/conf-data/blob/master/data/2011ICSE.json)  
📝 **Description:** wish is an AI-driven shell environment that translates natural language input into executable shell commands, streamlining penetration testing workflows. Traditional penetration testing heavily relies on memorizing commands or copying and pasting from references, which can be inefficient. wish enables security professionals to focus on strategy and situational awareness rather than syntax recall.

Beyond simple command translation, wish integrates a built-in knowledge base that provides contextual recommendations based on previous executions, making it a powerful assistant for both novice and expert penetration testers. It also seamlessly interacts with C2 frameworks, enabling post-exploitation activities such as privilege escalation, lateral movement, and persistence setup through natural language instructions. With its modular design, wish can be extended to support additional tools, making it a flexible and scalable solution for modern penetration testing workflows.

</details>

---
### 📅 2024
<details><summary><strong>ADOKit</strong> - By h4wkst3r</summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2024-blue)](https://www.blackhat.com/us-24/arsenal/schedule/index.html#adokit-azure-devops-services-attack-toolkit-38148)  
🔗 [GitHub](https://github.com/xforcered/ADOKit)  
📝 **Description:** Azure DevOps Services Attack Toolkit - ADOKit is a toolkit that can be used to attack Azure DevOps Services by taking advantage of the available REST API. The tool allows the user to specify an attack module, along with specifying valid credentials (API key or stolen authentication cookie) for the respective Azure DevOps Services instance. The attack modules supported include reconnaissance, privilege escalation and persistence. ADOKit was built in a modular approach, so that new modules can be added in the future by the information security community.

</details>

<details><summary><strong>Legion</strong> - By Adam Compton & Bill Harshbarger </summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2017-blue)](http://www.toolswatch.org/2017/06/the-black-hat-arsenal-usa-2017-phenomenal-line-up-announced/)  
🔗 [GitHub](https://github.com/MooseDojo/Legion)  
📝 **Description:** At its core, Legion is a distributed computing application. It is written in python and designed from the ground up to fulfill various IT related needs. Whether you need a way to logically distribute large or complex commands across multiple systems, or if you need a way to remotely administer 1 or more other systems, Legion can help. Legion goes beyond a typical Master/Manager/Slave architecture and makes use of a MeshNetworking approach to help to dynamically route around failed nodes and networking issues. Additionally, it has the ability to allow remote shell access to any node as well as send individual commands to 1 or all of the nodes within the mesh. And of course all the communications are encrypted between the nodes.

</details>

<details><summary><strong>Merlin</strong> - By Ne0nd0g </summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2018-blue)](https://www.toolswatch.org/2018/05/black-hat-arsenal-usa-2018-the-w0w-lineup)  
🔗 [GitHub](https://github.com/Ne0nd0g/merlin)  
📝 **Description:** Merlin is a cross-platform post-exploitation HTTP/2 Command & Control server and agent written in golang.
An introductory blog post can be found [here](https://medium.com/@Ne0nd0g/introducing-merlin-645da3c635a)

</details>

<details><summary><strong>SCMKit</strong> - By Hawkins </summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2022-blue)](https://www.blackhat.com/us-22/arsenal/schedule/index.html#scmkit-source-code-management-attack-toolkit-26592)  
🔗 [GitHub](https://github.com/xforcered/SCMKit)  
📝 **Description:** Source Code Management Attack Toolkit - SCMKit is a toolkit that can be used to attack SCM systems. SCMKit allows the user to specify the SCM system and attack module to use, along with specifying valid credentials (username/password or API key) to the respective SCM system. Currently, the SCM systems that SCMKit supports are GitHub Enterprise, GitLab Enterprise and Bitbucket Server. The attack modules supported include reconnaissance, privilege escalation and persistence. SCMKit was built in a modular approach, so that new modules and SCM systems can be added in the future by the information security community.

</details>

<details><summary><strong>ShinoBOT Family</strong> - By Sh1n0g1 </summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2016-blue)](https://www.toolswatch.org/2016/06/the-black-hat-arsenal-usa-2016-remarkable-line-up)  
🔗 [GitHub](https://github.com/Sh1n0g1/ShinoBOT)  
📝 **Description:** ShinoBOT Family is a malware set to test the security solution / security posture of the organization.

</details>

<details><summary><strong>WarBerryPi</strong> - By Yiannis Ioannides </summary>

📅 **Presented:** [![Tools](https://img.shields.io/badge/Black_Hat_Tools-USA_2016-blue)](https://www.toolswatch.org/2016/06/the-black-hat-arsenal-usa-2016-remarkable-line-up/)  
🔗 [GitHub](https://github.com/secgroundzero/warberry)  
📝 **Description:** WarBerryPi was built to be used as a hardware implant during red teaming scenarios where we want to obtain as much information as possible in a short period of time with being as stealth as possible. Just find a network port and plug it in. The scripts have been designed in a way that the approach is targeted to avoid noise in the network that could lead to detection and to be as efficient as possible. The WarBerry script is a collection of scanning tools put together to provide that functionality.
</details>



## 📌 Notes

- This list will be updated as more Red Teaming tools are parsed from additional years and locations.
- All entries are sorted by tool name for clarity.
- Want to contribute? Open a PR on the [GitHub repository](https://github.com/UCYBERS/Awesome-BlackHat-Tools).

---

