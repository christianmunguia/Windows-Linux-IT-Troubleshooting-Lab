# Windows-Linux-IT-Troubleshooting-Lab
## Overview

This home lab simulates six common IT help desk incidents involving Windows 11 and Ubuntu Linux. I built the environment using VirtualBox and used osTicket to manage incidents as a help desk technician woukd.

Each scenario documetns the reported problem, the commands and tools I used to investigate it, what I found, how I resolved it, and how I verified the fix.


## Lab Environment

| Technology | Purpose |
|---|---|
| Windows 11 | Windows client administration and troubleshooting |
| Ubuntu 25.10 | Linux administration and networking |
| Oracle VirtualBox | Virtualization and virtual networking |
| osTicket | Help desk ticket management and documentation |
| Remmina | RDP client for remote desktop troubleshooting |
| OpenSSH | linux SSH remote access |
| Powershell/Command Prompt | Windows diagnostic and configuration |
| Linux Terminal | Linux networking and service diagnostics |


## Troubleshooting Scenarios

| Ticket | Issue | Root Cause and Resolution |
|---|---|---|
| 01 | RDP / Remmina Connection Failure | A restrictive RDP policy (`fDenyTSConnections=1`) disabled Remote Desktop, and no RDP listener was active. Removed the policy restriction, restored the RDP listener, and verified remote access. |
| 02 | Ubuntu DNS Resolution Failure | An incorrect DNS server prevented domain names from resolving. Restored the correct DNS server and verified name resolution. |
| 03 | Windows Proxy Configuration Issue | Incorrect proxy settings prevented websites from loading. Corrected the proxy configuration and confirmed access was restored. |
| 04 | Windows NTFS Permissions Issue | Missing folder permissions and disabled file inheritance prevented access. Restored read access and re-enabled inheritance. |
| 05 | Windows Network Connectivity Failure | An incorrect static default gateway prevented external connectivity. Restored DHCP and verified network access. |
| 06 | Linux SSH Service Failure | The SSH service and socket were stopped. Started the SSH socket and confirmed remote access worked. |

## Troubleshooting Approach

I used diagnostic tools to narrow down each problem before making changes.

For networking issues, I checked IP configuration, connectivity, DNS resolution, and routing as appropriate. For remote access problems, I investigated listening ports, service status, firewall rules, and system configuration.

I used tools such as ping, ipconfig, netstat, qwinsta, Test-NetConnection, icacls, route print, tracert, nslookup, resolvectl, systemctl, and ss to diagnose issues and verify results.

After applying a fix, I retested the original problem and documented the findings and resolution in osTicket.

## Skills Demonstrated

- Windows 11 and Ubuntu Linux troubleshooting
- TCP/IP networking, DNS, routing, and proxy configuration
- RDP and SSH remote access troubleshooting
- Windows Registry and service administration
- NTFS permissions and inheritance
- Windows and Linux command-line diagnostics
- Root cause analysis and problem resolution
- Help desk ticket management using osTicket
- Technical documentation and verification

## Project Documentation

- Each of the six incidents has a separate technical writeup covering:
- Issue description and lab setup
- Troubleshooting steps and diagnostic findings
- Root cause and resolution
- Verification and prevention
- Supporting screenshots

See the tickets/ directory for individual troubleshooting writeups and the screenshots/ directory for supporting evidence.

## Project Scope

This project was completed in a controlled home lab using virtual machines and simulated help desk incidents. It demonstrates hands-on troubleshooting and documentation practices rather than production IT support experience.

