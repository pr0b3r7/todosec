---
description: 'Encountered this issue on 4/10/2021, fixed it with'
---

# AutoBlue-MS17-010 pip2.7 Impacket issue

![&quot;pip2.7 install -r requirements.txt&quot; = error installing requirements.txt for AutoBlue-MS17-010](../../../../.gitbook/assets/autoblue-ms17-010-pip2.7-requirements-error.png)

Today, encountered an issue with Impacket's installation In order to fix, run "_pip2.7 install --upgrade setuptools_"

![Issue seems to be related to setuptools being out of date](../../../../.gitbook/assets/autoblue-ms17-010-pip2.7-requirements-setuptools-fix.png)



