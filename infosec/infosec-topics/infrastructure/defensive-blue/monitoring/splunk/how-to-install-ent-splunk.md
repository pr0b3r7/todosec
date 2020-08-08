---
description: Developer License program
---

# How to install Enterprise Splunk

Hi Team, 

Let's _**Splunk**_ for fun and profit, and most importantly for FREE. Head [here](https://dev.splunk.com/enterprise/dev_license). At the time of writing you would land in the following website: 

![Splunk Dev License Signup](../../../../../../.gitbook/assets/image%20%2864%29.png)

Developer license allows us to install a Splunk deployment to write our own apps, get familiar with their architecture and I imagine they are trying to build and ecosystem for their app... 

[Download Link - Splunk Enterprise](https://www.splunk.com/download)

After installing, you will find your dashboard navigating to localhost:8000/en-US/app/launcher/home from your browser: 

![Default view, no dashboard configured... yet. ](../../../../../../.gitbook/assets/image%20%2865%29.png)

After navigating to New Search, we can see some data being retrieved by the index. As a matter of fact, that is all this section is for. 

![Search Section ](../../../../../../.gitbook/assets/image%20%2862%29.png)

**Troubleshooting:**

**If we were to have issues or cannot browse to Splunk Server at https://localhost:8000/ or the page does not load we have a few options to diagnose the issue:**

![Troubleshooting shows page loads OK!](../../../../../../.gitbook/assets/image%20%2863%29.png)

1 - Command line and check for open port **8000/tcp** 

To open the command line: **WIN + X &gt; CMD**

2 - Chrome Developer console **- We want to see HTTP/200 code - "OK"** upon refreshing \(F5 or Ctrl + R\) 

