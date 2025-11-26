# Network Configuration (VMware NAT)

## Overview
All virtual machines in this lab are connected through a VMware NAT network.  
This allows internal communication while keeping them isolated from the public internet.

## Virtual Machine IP Summary
| Machine            | IP Address        | Purpose                     |
|-------------------|-------------------|-----------------------------|
| Kali Linux        | 192.168.113.128   | Attacker / Tools           |
| Ubuntu Server     | 192.168.113.131   | Admin / Logging / SSH      |
| Metasploitable 2  | 192.168.113.132   | Vulnerable Target Machine  |

## Connectivity Tests trying ping others ip address

### Kali → Others
### Ubuntu → Others
### Metasploitable → Others


All successful → Network verified.

## Notes
ICMP response was enabled on Metasploitable to allow bidirectional ping.


