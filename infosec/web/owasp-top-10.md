---
description: >-
  Open Web Application Security Project's top 10 most important web application
  security risks. Updated every 3 years by OWASP
---

# OWASP TOP 10

![Minimize these risks to reduce web application vulnerabilities](../../.gitbook/assets/image%20%2859%29.png)

## A1:2017 - Injection

Injection flaws such as SQL, NoSQL, OS, or LDAP occur when non-trustworthy data is sent to an interpreter, as part of a command or query. The malign data may manipulate the interpreter into executing arbitrary logic or provide access to resources without using the appropriate authentication mechanisms.

## A2:2017 - Broken Authentication

Functions in the application related to authentication and management of sessions are implemented wrongly, allowing a malicious user to compromise the username and passwords, session tokens, or exploiting other flaws in the implementation to assume the identity of other users \(may that be permanent or temporary\).

## A3:2017 - Sensitive Data Exposure

Many web applications and [Application Programmable Interfaces \(APIs\)](https://www.freecodecamp.org/news/what-is-an-api-in-english-please-b880a3214a82/) do not provide adequate protection for sensitive data. Sensitive data may be financial, health, or [Personally Identifiable Information \(PII - linked definition by the U.S Department of Labor\)](https://www.dol.gov/general/ppii#:~:text=Personal%20Identifiable%20Information%20%28PII%29%20is,either%20direct%20or%20indirect%20means.&text=It%20is%20the%20responsibility%20of,to%20which%20they%20have%20access.). The attacker could steal or modify the inadequately protected data to commit fraudulent operations with credit cards, identity theft u other crimes. Sensitive data require additional protection methods such as during transit and at rest ciphering.

## A4:2017 - External XML Entities \(XXE\)

Many legacies or misconfigured XML processors evaluate references to external entities in XML documents. These external entities may be used to reveal internal files through the [URI \(Uniform Resource Identifiers\)](https://www.iana.org/assignments/uri-schemes/uri-schemes.xhtml) or in outdated servers, perform port-scanning in their LAN, remote arbitrary code execution, and perform Denial of Service \(DoS\) attacks.

## A5:2017 - Broken Access Control _\(A4:2013 - Insecure Direct Object References + A7:2013 - Missing Function Level Access Control\)_

When restrictions over what authenticated users can do are not applied correctly, attackers may exploit these circumstances to unauthorizedly ****access functionalities and/or data, other users' accounts, read sensitive data, modify data, change access rights and permissions, etc. 

## A6:2017 - Security Misconfiguration

The very common issues mainly caused due to manually, ad hoc, or lack thereof configuration. i.e: open S3 buckets, misconfigured HTTP headers, error messages revealing sensitive data, lack of patches and updates, outdated frameworks, deprecated dependencies, and components.

## A7:2017 - Cross-Site Scripting \(XSS\)

XSS occurs when applications intake non-trustworthy data and send it to the web browser without proper validation nor codification; or when it updates the existing webpage with data provided by the user using the _JavaScript-consuming_ [API ](https://www.youtube.com/watch?v=s7wmiS2mSXY)in the browser.  XSS allows attackers to execute commands in the victim's browser and the attacker may hijack the session, modify \([defacement](https://documents.trendmicro.com/assets/white_papers/wp-a-deep-dive-into-defacement.pdf)\) websites or redirect users to a malicious website. 

## A8:2017 - Insecure Deserialization

These defects occur when an application receives damaged serialized objects and these objects may be manipulated or deleted by the attacker to perform repetition, injection, or execution privilege escalation. In the worst cases, insecure deserialization may be conducive to remote arbitrary code execution on the target server.

## A9:2017 - Using Components With Known Vulnerabilities

Some components like libraries, frameworks, and other modules, are executed with the same privileges as the application. If a vulnerable component is exploited, the attacker could cause a loss of data or take control over the server. The applications and API that leverage components with known vulnerabilities could weaken the application defense and allow diverse attacks and unintended impacts.

## A10:2017 - Insufficient Logging and Monitoring

Insufficient logging and monitoring, alongside the lack of response in the event of incidents, allow attackers to maintain access, privileges, manipulate, extract, and even destroy data. Studies report that the average security breach detection time is over 200 days, being typically detected by third parties instead of through internal processes. As you can imagine, this would imply that the damage has been long done.

