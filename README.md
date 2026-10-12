<h1> Windows Enumeration for Privilege Escalation </h1>

### 🔹Leve1-WinEnum.ps1

> 1. System & Host Enumeration
>
> 2. User & Session Enumeration
>   
> 3. AV status and Security Configuration
>
> 4. Credential & Sensitive data exposure discovery
>
> 5. Privilege Escalation & Permission Enumeration
>
> 6. Software & Patch Enumeration

Developed in PowerShell for local reconnaissance, gathering system information, and identifying potential configuration flaws that could present opportunities for privilege escalation during Red Team operations. Its primary function is to gather information (host enumeration) about the Windows environment, user accounts and sessions, access permissions, security mechanisms, and system settings.

#### Important:

- It's not an exploit: the script mainly performs local queries and checks.
- The results require validation: some checks depend on permissions, the Windows version, the availability of modules, and the interpretation of registry values
- New features are being added over time

#

### 🔹LookForCredentials.ps1

> 1. Recursive File System Enumeration
>
> 2. Credential & Secret Discovery
> 
> 3. Sensitive File Scanning & Findings Collection

This script specializes in locating potential credentials and authentication information exposed in text and configuration files on the Windows file system.
It searches for text patterns associated with passwords, tokens, API keys, usernames, and other potentially sensitive information.

#### Important:

The script is designed to assist professionals. It does not automatically extract credentials from memory, decrypt files, or perform authentication or exploitation. Because it uses generic patterns, it may produce false positives and miss credentials that do not match the implemented regular expressions. A careful, human review is required.

#

### 🔹ManifestsCheck.ps1

> 1. PE Resource Enumeration & Manifest Extraction
>
> 2. XML Parsing & Formatting

`Manifests-Check.ps1` is a Windows Application Manifest Inspection tool, developed in PowerShell with integration into the native Windows API via C#. Its purpose is to extract, parse, and display the XML manifest embedded in executable files and other files compatible with PE (Portable Executable) resources. Windows manifests may contain settings that are important for a security analysis

#### Important:

The script does not recursively search for executables, does not list processes, does not automatically identify vulnerabilities, and does not perform exploitation. A professional review should be conducted while using it.

# Warning!
I wrote this set of scripts to help me and my colleagues in some way during a real-world operation or CTF. It was developed in environments that I tested and controlled; it does not encourage irresponsible use and is intended solely for security professionals. Feel free to modify or edit the script to meet your needs.
