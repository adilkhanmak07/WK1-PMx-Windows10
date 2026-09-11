# WK1-PMx — Windows 10 VirtualBox Lab

## Overview

This project demonstrates the deployment and network configuration of a **Windows 10 virtual machine using Oracle VirtualBox** as part of a Week 1 practical networking lab.

The lab focused on installing Windows 10, configuring a static IPv4 address, connecting the VM to the required NAT Network, and verifying communication between Windows 10 and Kali Linux.

---

## Objectives

* Deploy a Windows 10 virtual machine in VirtualBox
* Install Windows 10 using an ISO image
* Configure the VM to use a NAT Network
* Configure a static IPv4 address
* Establish connectivity with Kali Linux
* Verify internet connectivity
* Troubleshoot ICMP connectivity issues
* Document the complete lab configuration

---

## Lab Environment

| Component               | Configuration     |
| ----------------------- | ----------------- |
| Virtualization Platform | Oracle VirtualBox |
| Operating System        | Windows 10        |
| Network Type            | NAT Network       |
| Network                 | `10.0.0.0/24`     |
| Gateway                 | `10.0.0.1`        |
| DNS                     | `8.8.8.8`         |
| Kali Linux              | `10.0.0.2`        |
| Windows 10              | `10.0.0.10`       |

---

## Virtual Machine Configuration

The Windows 10 virtual machine was created with the following configuration:

* **VM Name:** Windows10-Lab
* **Operating System:** Microsoft Windows 10 (64-bit)
* **Memory:** 4096 MB RAM
* **Virtual Disk:** VDI
* **Disk Allocation:** Dynamically allocated
* **Disk Size:** 40 GB or more
* **Network Adapter:** NAT Network

The Windows 10 ISO was attached to the VM and the operating system was successfully installed.

---

## Network Configuration

The Windows 10 VM was connected to the same NAT Network as the Kali Linux VM.

### Windows 10 IPv4 Configuration

```text
IP Address:      10.0.0.10
Subnet Mask:     255.255.255.0
Default Gateway: 10.0.0.1
Preferred DNS:   8.8.8.8
```

### Kali Linux

```text
IP Address:      10.0.0.2
Network:         10.0.0.0/24
Gateway:         10.0.0.1
```

Both virtual machines were therefore configured on the same `10.0.0.0/24` network.

---

## Connectivity Verification

### Windows 10 → Kali Linux

Command:

```cmd
ping 10.0.0.2
```

**Result:** Successful.

Windows 10 successfully communicated with the Kali Linux VM.

### Windows 10 → Internet

Command:

```cmd
ping 8.8.8.8
```

**Result:** Successful.

This confirmed that the Windows 10 VM had internet connectivity.

### Kali Linux → Windows 10

Command:

```bash
ping -c 4 10.0.0.10
```

Final result:

```text
4 packets transmitted, 4 received, 0% packet loss
```

**Result:** Successful.

This confirmed communication from Kali Linux to the Windows 10 VM.

---

## Troubleshooting

During the initial connectivity test, Kali Linux could not reach the Windows 10 VM:

```text
4 packets transmitted, 0 received, 100% packet loss
```

The Windows Firewall configuration was reviewed and the appropriate **ICMP Echo Request** inbound rule was enabled.

The connectivity test was then repeated:

```bash
ping -c 4 10.0.0.10
```

The final test completed successfully with **0% packet loss**.

This demonstrated basic troubleshooting of Windows Firewall and ICMP connectivity.

---

## Verification Summary

| Connectivity Test       | Result       |
| ----------------------- | ------------ |
| Windows 10 → Kali Linux | ✅ Successful |
| Windows 10 → Internet   | ✅ Successful |
| Kali Linux → Windows 10 | ✅ Successful |
| Final Packet Loss       | ✅ 0%         |

---

## Skills Demonstrated

* Oracle VirtualBox
* Windows 10 deployment
* Virtual machine configuration
* NAT Network configuration
* IPv4 addressing
* Static IP configuration
* DNS and gateway configuration
* ICMP connectivity testing
* Windows Firewall troubleshooting
* Basic Windows and Linux networking
* Technical documentation

---

## Conclusion

The Windows 10 virtual machine was successfully deployed and configured in Oracle VirtualBox.

The required static network configuration was applied, connectivity between Windows 10 and Kali Linux was verified in both directions, and internet connectivity was confirmed.

An initial ICMP connectivity issue was also identified and resolved through Windows Firewall troubleshooting.

**Lab Status: Completed ✅**
