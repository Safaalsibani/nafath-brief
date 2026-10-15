Version: NAFATH-V4
Track: Software

## Overview

Securing the software supply chain of a national service provider requires a coordinated strategy to protect the integrity, reliability, and trustworthiness of interconnected digital services. Six IT disciplines contribute complementary controls: Software Engineering separates sensitive credentials from source code; Artificial Intelligence security addresses attacks on model behavior and information; Mobile security verifies applications against defined security requirements; Networking protects routing integrity against unauthorized traffic redirection; Cybersecurity identifies and remediates vulnerable software dependencies; and Data Management improves component transparency through Software Bills of Materials (SBOMs). Together, these practices improve visibility into supply-chain risks, support informed security decisions, and strengthen the resilience of essential digital services.

## Software
The Twelve-Factor App methodology recommends storing deployment-specific configuration, including database credentials, API keys, and secrets, in environment variables rather than source code. This separation reduces accidental exposure through version control and allows the same application build to use different settings across development, testing, and production. However, environment variables alone do not guarantee confidentiality. Access controls, secure secret storage, and credential rotation remain essential safeguards. This approach improves deployment flexibility while reducing credential-leakage risks.

Resource: The Twelve-Factor App - III. Config - https://12factor.net/config
## AI
NIST identifies adversarial machine-learning threats including evasion, poisoning, privacy attacks, and AI misuse or abuse. Evasion manipulates inputs during inference to cause incorrect predictions without modifying the trained model. Poisoning alters training data or model updates, compromising learning. Privacy attacks attempt to expose sensitive information, while misuse or abuse exploits AI capabilities for harmful purposes. Understanding these differences helps security teams identify where attacks occur and choose appropriate protections throughout the AI lifecycle.

Resource: Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://www.nist.gov/publications/adversarial-machine-learning-taxonomy-and-terminology-attacks-and-mitigations-0
## Mobile
The OWASP Mobile Application Security Verification Standard (MASVS) defines security requirements across eight areas: storage, cryptography, authentication and authorization, network communication, platform interaction, code quality, resilience, and privacy. To assess an application, security teams select relevant MASVS controls, perform appropriate tests, record evidence, and compare findings against the requirements. They then remediate weaknesses and retest the affected controls. Used alongside practical testing guidance, MASVS provides a repeatable, evidence-based process for evaluating mobile application security.

Resource: OWASP - Mobile Application Security Verification Standard - https://mas.owasp.org/MASVS/
## Networking
BGP route hijacking occurs when unauthorized or more-specific route announcements attract traffic away from its intended destination. RPKI provides signed Route Origin Authorizations (ROAs) identifying which Autonomous Systems may originate IP prefixes. Routers using Route Origin Validation (ROV) can reject announcements with invalid origins when configured to do so. However, RPKI origin validation does not verify the complete AS_PATH and cannot prevent all route hijacking or path manipulation attacks.

Resource: RFC 6811 - BGP Prefix Origin Validation - https://www.rfc-editor.org/rfc/rfc6811
## Cybersecurity
Log4Shell (CVE-2021-44228) was a critical vulnerability in Apache Log4j 2's log4j-core component. Attacker-controlled log messages could trigger unsafe JNDI lookups and remote code execution. Its CVSS 3.1 score of 10.0 reflected network exploitability, low attack complexity, and no required privileges. Apache initially fixed the issue in version 2.15.0 for Java 8, but related vulnerabilities prompted additional updates. The recommended response is to identify affected installations and upgrade to a supported, fully patched release.

Resource: Apache Logging Services - Security - https://logging.apache.org/security.html
## Data
A Software Bill of Materials (SBOM) is a machine-readable inventory of software components and their dependencies. The 2026 Minimum Elements guidance specifies component producer, name, version, identifiers, license, dependency relationships, and cryptographic hash values and algorithms. It also includes SBOM author, timestamp, document version, data format, generation context, tools, and signature information. These fields enable component tracking and faster vulnerability investigations. However, an SBOM supports risk assessment rather than proving that software is secure.

Resource: 2026 Minimum Elements for a Software Bill of Materials (SBOM) - https://www.cyber.gov.au/publication/2026-minimum-elements-for-a-software-bill-of-materials-sbom
## Misconception in My Track

## Open Question
