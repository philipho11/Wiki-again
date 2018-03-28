ITS pre-configures several VM with the following common properities:
* complienanced with HKU server complience policy, with IEM agent installed
* Linux's default user is "cloud-user"
* Microsoft Window's default user is "Administrator"
* Microsoft Window installed with Sophos Antivirus
* SSH/remote desktop is limited to HKU IP by built-in firewall rules

***

The following images are pre-configured by ITS:
* its-global-centos7-autofs: pre-configured CentOS 7 image, "/" with auto-enlarge to fully utilize the disk during the first boot
* its-global-centos7: pre-configured CentOS 7 image, uses just 4 GB. If the disk assigned large than 4GB, you need to enlarge / create partition manually with the free unused diskspace
* its-global-win206: pre-configured Microsoft Window Server 2016, uses just X GB. If the disk assigned large than 4GB, you need to enlarge / create partition manually with the free unused diskspace
* its-internal-centos7: pre-configured CentOS 7 image, available to ITS internal only. Same configuration as its-global-centos7, but with
  + more restricted firewall rule, hosts.allow to limite the access to ITS developer subnet
  + PMS ready
  + splunk client ready
  + HP DP agent ready
  + sysmon client ready
  + nagios client ready
* its-internal-win206: pre-configured Microsoft Window Server 2016, available to ITS internal only. Same configuration as its-global-2016, but with
  + more restricted firewall rule, hosts.allow to limite the access to ITS developer subnet
  + PMS ready
  + splunk client ready
  + HP DP agent ready
  + sysmon client ready
  + nagios client ready
