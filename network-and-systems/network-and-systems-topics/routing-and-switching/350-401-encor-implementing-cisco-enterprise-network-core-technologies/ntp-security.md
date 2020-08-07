# NTP Security

NTP is used to synchronize network devices/computer system time settings. Without NTP, computers would slowly drift away from each other in time. Eventually there would be a lot of differences between the clocks, even within one network of devices. For systems that require events to occur at a certain intervals, this is an issue. In terms of troubleshooting any network issues, having varying times on devices can make it hard to determine what time an outage approximately occurred. One device may show it received a reply much slower than expected due to time differences on the computers.

#### Why is NTP security important?

* You only want to use time settings from trusted sources
* An attacker may broadcast wrong time stamps
* An attacker may be disguised as another time server

To ensure the device receives the correct settings, we must ensure it is contacting the correct NTP server. For this, we can use authentication. NTP authentication uses a key, a password you create so make it strong. This key must be known and trusted between the server and the clients. Authentication does not involve any kind of encryption. The key attached to the device's data acts as a digital signature that the other device, having the same key, can match and confirm they are reaching the correct server.

#### [Configuration of NTP](https://www.cisco.com/c/en/us/td/docs/routers/crs/software/crs_r4-3/system_management/command/reference/b_sysman_cr43crs/b_sysman_cr43crs_chapter_01011.html)

| Command | Utility |
| :--- | :--- |
| _ntp master 10_ |  |
| _show clock detail_ | to verify source is ntp & time is correct |
| ntp server x.x.x.x  | specify ip address of ntp server |

#### Security Configuration



| Command | Utility |
| :--- | :--- |
| _ntp authenticate_  |  |
| _ntp authentication-key x md5 xxxx_ |  |
| _ntp server x.x.x.x key x_ |  |

#### NTP Commands

| Command | Utility |
| :--- | :--- |
| _show ntp status_ | to view devices current ntp status, stratum, reference, etc |
| _show ntp associations_ | to view if device has ntp master, OR AS MASTER: master ip, whether they are synced, metrics |

