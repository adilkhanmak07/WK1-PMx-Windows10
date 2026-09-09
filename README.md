# \# WK1-PMx — Windows 10 VirtualBox Lab

# 

# \## Project Overview

# 

# This project documents the complete setup and configuration of a Windows 10 virtual machine in Oracle VirtualBox.

# 

# The objective is to build a Windows 10 lab environment, connect it to the same VirtualBox NAT Network used by the Kali Linux machine, configure the required network settings, and verify communication between both systems and the internet.

# 

# The project also focuses on documenting the actual setup process with screenshots, identifying any missing or incorrect instructions in the provided guide, and producing a final demonstration video.

# 

# \## Objectives

# 

# \* Obtain the official Windows 10 ISO from Microsoft.

# \* Create and configure a Windows 10 virtual machine in VirtualBox.

# \* Install Windows 10 using the downloaded ISO.

# \* Connect Windows 10 to the existing VirtualBox NAT Network.

# \* Configure the required IPv4 settings.

# \* Verify Windows 10 connectivity with Kali Linux.

# \* Verify internet connectivity from Windows 10.

# \* Verify connectivity from Kali Linux to Windows 10.

# \* Document each relevant setup stage with screenshots.

# \* Correct and improve the original setup instructions where required.

# \* Record a complete Windows 10 VM setup demonstration.

# 

# \## Lab Environment

# 

# | Component         | Configuration          |

# | ----------------- | ---------------------- |

# | Hypervisor        | Oracle VirtualBox      |

# | Operating System  | Windows 10 64-bit      |

# | Kali Linux        | Existing lab VM        |

# | Network Type      | VirtualBox NAT Network |

# | Kali Linux IP     | 10.0.0.2/24            |

# | Windows 10 IP     | 10.0.0.10/24           |

# | Gateway           | 10.0.0.1               |

# | DNS               | 8.8.8.8                |

# | Windows VM Memory | 4096 MB                |

# | Windows VM Disk   | 40 GB minimum          |

# | IP Configuration  | Static IPv4            |

# 

# \## Repository Structure

# 

# ```text

# WK1-PMx-Windows10/

# │

# ├── README.md

# │

# ├── Guide/

# │   └── Windows10-VM-Setup-Guide.md

# │

# ├── Screenshots/

# │

# ├── Video/

# │

# └── Documentation/

# &#x20;   └── Screenshot-Checklist.md

# ```

# 

# \### Directory Purpose

# 

# \* \*\*Guide/\*\* — Final tested and corrected Windows 10 setup guide.

# \* \*\*Screenshots/\*\* — Evidence captured during each stage of the setup.

# \* \*\*Video/\*\* — Final Windows 10 VM setup demonstration.

# \* \*\*Documentation/\*\* — Supporting project documentation and checklists.

# 

# \## Setup Process

# 

# The project is completed in the following stages:

# 

# 1\. Download the official Windows 10 ISO.

# 2\. Create the Windows 10 virtual machine.

# 3\. Attach the ISO and install Windows 10.

# 4\. Configure the VirtualBox NAT Network.

# 5\. Configure the Windows 10 static IPv4 address.

# 6\. Test Windows-to-Kali and internet connectivity.

# 7\. Test Kali-to-Windows connectivity.

# 8\. Complete the documentation and final evidence.

# 

# \## Network Verification

# 

# Successful completion requires verification of:

# 

# ```text

# Windows 10 → Kali Linux

# 10.0.0.10 → 10.0.0.2

# 

# Windows 10 → Internet

# 10.0.0.10 → 8.8.8.8

# 

# Kali Linux → Windows 10

# 10.0.0.2 → 10.0.0.10

# ```

# 

# The corresponding screenshots are stored in the `Screenshots/` directory.

# 

# \## Documentation Approach

# 

# The original Windows 10 setup guide is being followed and tested step by step rather than reproduced without verification.

# 

# Where a step is incomplete, unclear, or technically incorrect, the procedure will be updated based on the actual working configuration.

# 

# Screenshots are captured as evidence during the implementation and matched to the relevant instructions in the final guide.

# 

# \## Project Status

# 

# \*\*Status:\*\* In Progress

# 

# The repository structure and documentation workflow have been established. The Windows 10 virtual machine setup and evidence collection will be documented as the project progresses.

# 

# \## Final Deliverables

# 

# \* Corrected Windows 10 VirtualBox setup guide

# \* Step-by-step screenshots

# \* Screenshot checklist

# \* Windows 10 VM setup demonstration video

# \* Git/GitHub project history



