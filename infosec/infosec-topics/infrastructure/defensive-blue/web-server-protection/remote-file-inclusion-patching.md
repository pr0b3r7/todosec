# Remote File Inclusion Patching

To an extent, you can minimize the risk of RFI attacks through proper input validation and sanitization. However, when you do, it is important to avoid the misconception that all user inputs can be completely sanitized. As a result, sanitization should only be considered a supplement to a dedicated security solution.

Having said that, it’s always preferable to sanitize user-supplied/controlled inputs to the best of your ability. These inputs include:

* GET/POST parameters
* URL parameters
* Cookie values
* HTTP header values

In the process of sanitization, input fields should be checked against a whitelist \(allowed character set\) instead of a blacklist \(disallowed malicious characters\). Generally speaking, blacklist validation is considered a weak solution, as attackers can choose to supply input in a different format, such as encoded or hexadecimal formats.

It’s also best practice for output validation mechanisms to be applied on the server end. Client-side validation functions, having the benefit of reducing processing overhead, are also vulnerable to attacks by proxy tools.

Finally, you should consider restricting execution permission for the upload directories and maintain a whitelist of allowable file types \(for example PDF, DOC, JPG, etc.\), while also restricting uploaded file sizes.

[Source](https://www.imperva.com/learn/application-security/rfi-remote-file-inclusion/)

