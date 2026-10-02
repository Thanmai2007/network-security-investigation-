# Network Security Investigation Using Linux Tools

## Project Overview

This project presents a Mini Security Operations Center (SOC)-style investigation lab developed in a controlled Kali Linux environment.

The project demonstrates a structured approach to network security investigation using Nmap, Ncat, Wireshark, and Linux networking utilities.

The investigation focuses on a local system using the loopback address `127.0.0.1` and a controlled TCP connection on port `4444`.

## Objectives

- Perform network reconnaissance using Nmap.
- Identify the state of a selected TCP port.
- Generate controlled TCP communication using Ncat.
- Monitor listening and established connections using `ss`.
- Capture and analyse TCP traffic using Wireshark.
- Identify associated processes using `ps`.
- Correlate evidence from network and system-level observations.
- Perform final verification after the test communication is stopped.
- Document the investigation findings.

## Tools Used

- Kali Linux
- Nmap
- Ncat
- Wireshark
- `ip addr`
- `ip route`
- `ss`
- `ps`

## Investigation Environment

- Operating System: Kali Linux
- Virtualization: VMware Workstation
- Target: Localhost
- IP Address: `127.0.0.1`
- Test TCP Port: `4444`
- Wireshark Interface: `lo`
- Wireshark Filter: `tcp.port == 4444`

## Investigation Workflow

1. Baseline network scan using Nmap.
2. Creation of a temporary Ncat TCP listener on port 4444.
3. Verification of the listening port using `ss`.
4. Nmap service and port verification.
5. Generation of controlled TCP communication using Ncat.
6. Monitoring of the established connection using `ss`.
7. Identification of Ncat processes using `ps`.
8. Capture and analysis of TCP packets using Wireshark.
9. Correlation of network and process-level evidence.
10. Final Nmap verification after stopping the Ncat communication.
11. Documentation of observations and evidence.

## Evidence and Investigation Activities

### Network Reconnaissance

Nmap was used to examine the local system and verify the state of TCP port 4444 during the controlled investigation.

### TCP Communication

Ncat was used to create a temporary TCP listener on port 4444 and generate controlled local TCP communication.

### Connection Monitoring

The Linux `ss` command was used to identify listening and established TCP connections associated with the controlled communication.

### Packet Analysis

Wireshark was used on the loopback interface to capture and analyse traffic associated with TCP port 4444.

Display filter used:

```text
tcp.port == 4444

