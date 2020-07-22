---
description: >-
  Open Web Application Security Project's top 10 most important web application
  security risks. Updated every 3 years by OWASP
---

# OWASP TOP 10

![Minimize these risks to reduce web application vulnerabilities](../../.gitbook/assets/image%20%2859%29.png)

## A1:2017 - Injection

Injection flaws such as SQL, NoSQL, OS, or LDAP occur when non trustworthy data is sent to an interpreter, as part of a command or query. The malign data may manipulate the interpreter into executing arbitrary logic or provide access to resources without using the appropriate authentication mechanisms.

## A2:2017 - Broken Authentication

Functions in the application related to authentication and management of sessions are implemented wrongly, allowing a malicious user to compromise the username and passwords, session tokens, or exploiting other flaws in the implementation to assume the identity of other users \(may that be permanent or temporary\).

## A3:2017 - Sensitive Data Exposure

Many web applications and [Application Programmable Interfaces \(APIs\)](https://www.freecodecamp.org/news/what-is-an-api-in-english-please-b880a3214a82/) do not provide adequate protection for sensitive data. Sensitive data may be financial, health or [Personally Identifiable Information \(PII - linked definition by the U.S Department of Labor\)](https://www.dol.gov/general/ppii#:~:text=Personal%20Identifiable%20Information%20%28PII%29%20is,either%20direct%20or%20indirect%20means.&text=It%20is%20the%20responsibility%20of,to%20which%20they%20have%20access.). The attacker could steal or modify the inadequately protected data to commit fraudulent operations with credit cards, identity theft u other crimes. Sensitive data require additional protection methods such as during transit and at rest ciphering.

## A4:2017 - External XML Entities \(XXE\)

Many legacy or misconfigured XML processors evaluate references to external entities in XML documents. These external entities may be used to reveal internal files through the [URI \(Uniform Resource Identifiers\)](https://www.iana.org/assignments/uri-schemes/uri-schemes.xhtml) or in outdated servers, perform port-scanning in their LAN, remote arbitrary code execution, and perform Denial of Service \(DoS\) attacks.

## A5:2017 - Broken Access Control _\(A4:2013 - Insecure Direct Object References + A7:2013 - Missing Function Level Access Control\)_

Restrictions over what authenticated users are able to do may not be implemented correctly. Attackers may exploit these circumstances to access, unauthorizedly, functionalities and/or data, other users' accounts, read sensitive data, modify data, change access rights and permissions, etc. 

## A6:2017 - Security Misconfiguration

Very common issue mainly caused due to manually, ad hoc, or lack thereof configuration. i.e: open S3 buckets, misconfigured HTTP headers, error messages revealing sensitive data, lack of patches and updates, outdated frameworks, deprecated dependencies, and components.

