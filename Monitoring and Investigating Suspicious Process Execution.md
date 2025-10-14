## Introduction

In this lab, I explore how to use Sysmon and Splunk together to monitor and analyze system activity for potential security incidents.

Sysmon (System Monitor) is a Windows system service and device driver that logs detailed information about system events such as process creation, network connections, and file modifications. It is commonly used in digital forensics and threat hunting to provide deeper visibility into endpoint behavior.

On the other hand, Splunk is a powerful Security Information and Event Management (SIEM) platform that allows users to collect, index, and visualize logs from multiple sources. By forwarding Sysmon logs to Splunk, analysts can search, correlate, and visualize event data to detect suspicious patterns or anomalous behavior across systems.

## System graph

<img width="538" height="501" alt="image" src="https://github.com/user-attachments/assets/0db15b35-4cc8-4fe1-998e-b7f17b3b7f8f" />

## Prerequisites

1. Ubuntu Server with sudo privileges.
2. Splunk Universal Forwarder installed and configured to forward logs.
3. Sysmon for Linux installed for monitoring process creation.
 
## Configuration and Deployment



###
