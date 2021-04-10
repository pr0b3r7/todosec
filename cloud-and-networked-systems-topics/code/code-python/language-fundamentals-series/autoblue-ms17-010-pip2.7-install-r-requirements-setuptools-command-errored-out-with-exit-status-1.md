---
description: 'Encountered this issue on 4/10/2021, fixed it upgrading setuptools'
---

# AutoBlue-MS17-010 pip2.7 install -r requirements setuptools 'Command errored out with exit status 1'

![&quot;pip2.7 install -r requirements.txt&quot; = error installing requirements.txt for AutoBlue-MS17-010](../../../../.gitbook/assets/autoblue-ms17-010-pip2.7-requirements-error.png)

Today I encountered an issue where attempting to install all dependencies that [3ndG4me/AutoBlue-MS17-010](https://github.com/3ndG4me/AutoBlue-MS17-010) has, I would receive an error within the first dependency \([Impacket](https://github.com/SecureAuthCorp/impacket.git)\) 

Through a quick google search, I found:  

\*\*\*\*[**pypi UserWarning: Unknown distribution option: 'install\_requires'**](https://stackoverflow.com/questions/8295644/pypi-userwarning-unknown-distribution-option-install-requires)\*\*\*\*

The solution that did work for me was: 

![posting here since I&apos;m too n00b to have an opinion on stackoverflow \(thanks bots\)](../../../../.gitbook/assets/autoblue-ms17-010-pip2.7-requirements-setuptools-fix-stackoverflow.png)

In order to fix, run "_pip2.7 install --upgrade setuptools_"

![Issue seems to be related to setuptools being out of date](../../../../.gitbook/assets/autoblue-ms17-010-pip2.7-requirements-setuptools-fix.png)

God bless you!

