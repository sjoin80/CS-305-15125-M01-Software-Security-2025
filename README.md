# CS-305-15125-M01-Software-Security-2025
CS-305-15125-M01 Software Security 2025

Artemis Financial
Secure Software Vulnerability Assessment

A real-world security assessment of a financial services web application, focused on identifying risk, protecting sensitive data, and aligning secure coding practices with regulatory expectations.

Why This Project Matters

Financial applications are high-value targets for cyberattacks because they process sensitive personal and financial data. Even small security oversights can result in data breaches, financial loss, and regulatory consequences.

This project demonstrates how security vulnerabilities can be identified early in the development lifecycle through structured analysis, manual code review, and static testing. The assessment focuses on preventing exploitation before issues reach production, while supporting application modernization.

Client Background

Client: Artemis Financial
Industry: Financial Services
Application Type: Java-based RESTful web application

Artemis Financial provides services related to savings, retirement, insurance, and investment planning. The company required a secure application architecture that ensures confidentiality, integrity, and availability of customer data while adopting modern development practices.

Software Security Objectives

The primary security goals of this assessment were to:

Protect sensitive financial and personal information

Enforce secure communications using modern encryption standards

Identify risks introduced by legacy code and third-party libraries

Support modernization without weakening the security posture

Regulatory Considerations

This assessment aligns with regulatory and compliance expectations commonly applied to financial systems, including:

Gramm-Leach-Bliley Act (GLBA): Requires financial institutions to safeguard customer information through technical and administrative controls

PCI DSS: Relevant when processing or transmitting payment card data

GDPR: Applicable for international users and cross-border data handling

These regulations emphasize encryption, access control, auditing, and continuous vulnerability management.

Vulnerability Assessment Approach

A layered, defense-in-depth approach was used to evaluate the application, including:

Architecture and configuration review

API security and input validation analysis

Cryptography and secure communication evaluation

Error handling and logging inspection

Dependency and third-party library analysis

Both manual code inspection and static testing were applied to ensure comprehensive coverage.

Key Security Findings

The assessment identified several vulnerabilities that could impact application security if left unaddressed:

Hard-coded database credentials and use of overly privileged accounts

Outdated cryptographic dependency (bcprov-jdk15on version 1.46)

Insecure exception handling exposing stack traces

Weak data encapsulation and missing input validation

Overly permissive file upload configuration

Incomplete date and time handling logic

Static Testing and Dependency Analysis

Static analysis was performed using the OWASP Dependency-Check Maven plugin.

Initial scans used version 9.0.7, which produced limited results due to outdated configuration and NVD API access requirements

The findings highlighted the risk of outdated dependencies and the importance of maintaining current security tools

Future scans should use the latest OWASP Dependency-Check version with a configured NVD API key to ensure complete CVE reporting

Mitigation Strategy

The mitigation plan focused on reducing risk while maintaining application functionality:

Externalizing credentials and enforcing least-privilege access

Upgrading vulnerable dependencies to supported versions

Replacing stack trace output with structured logging

Implementing strict input validation and encapsulation

Reducing file upload limits and validating file types

Using Java’s java.time API for accurate and secure time handling

Tools and Secure Coding Practices Used

OWASP Dependency-Check

Maven dependency management

Manual code review

Secure coding best practices

Least-privilege and defense-in-depth principles

Portfolio Value

This project demonstrates my ability to:

Perform a structured vulnerability assessment on a real-world application

Identify and prioritize software security risks

Apply secure coding and mitigation strategies

Align technical security decisions with regulatory requirements

Communicate security findings clearly to both technical and non-technical stakeholders

This artifact represents work I would confidently share with future employers to demonstrate practical software security and risk assessment skills.

Artifact Included

Artemis Financial Vulnerability Assessment Report (Project One)

Intended Audience

Software engineers interested in secure coding practices

Security-focused development teams

Employers seeking candidates with hands-on software security experience

Optional Enhancements

To further strengthen this repository:

Add the assessment document to a /docs folder

Include static analysis screenshots if available

Tag the repository with: software-security, owasp, java, vulnerability-assessment, secure-coding
