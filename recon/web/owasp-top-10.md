---
description: >-
  Open Web Application Security Project's top 10 most important web application
  security risks. Updated every 3 years by OWASP
---

# OWASP TOP 10

![Minimize these risks to reduce web application vulnerabilities](../../.gitbook/assets/image%20%2859%29.png)

## A1:2017 - Injection

Injection flaws such as SQL, NoSQL, OS or LDAP occur when non trustworthy data is sent to an interpreter, as part of a command or query. The malign data may manipulate the interpreter into executing arbitrary logic or provide access to resources without using the appropriate authentication mechanisms.

## A2:2017 - Broken Authentication

Functions in the application related to authentication and management of sessions are implemented wrongly, allowing a malicious user to compromise the username and passwords, session tokens, or exploiting other flaws in the implementation to assume the identity of other users \(may that be permanent or temporarily\).

## A3:2017 - Sensitive Data Exposure

Many web applications and [Application Programmable Interfaces \(APIs\)](https://www.freecodecamp.org/news/what-is-an-api-in-english-please-b880a3214a82/) do not provide adequate protection for sensitive data. Sensitive data may be financial, health or [Personally Identifiable Information \(PII - linked definition by the U.S Department of Labor\)](https://www.dol.gov/general/ppii#:~:text=Personal%20Identifiable%20Information%20%28PII%29%20is,either%20direct%20or%20indirect%20means.&text=It%20is%20the%20responsibility%20of,to%20which%20they%20have%20access.). The attacker could steal or modify the inadequately protected data to commit fraudulent operations with credit cards, identity theft u other crimes. Sensitive data require additional protection methods such as during transit and at rest ciphering.

