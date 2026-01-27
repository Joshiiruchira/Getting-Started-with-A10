## Deployment Variants

| Deployment Type          | Description                                                                                                                                                                                  | Deployment Mode                  | Use Case                                              |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- | ----------------------------------------------------- |
| A10 Control Lite    | Designed for small-scale enterprises. Provides simplified deployment with lower infrastructure needs. Supports ADC and ADO. Other apps (CGN, SSLi, Gi-FW) may appear but are for trial only. | Standalone only                  | Up to **10 ADC** or **5 ADO/TPS** devices             |
| A10 Control Standard | Designed for large enterprises and service providers. Supports high availability and large-scale deployments.                                                                                | Standalone or **3-node cluster** | Large-scale ADC, CGN, ADO, SSLi, and GiFW deployments |

## Platform Requiremts

| Component  | Requirement                    |
| ---------- | ------------------------------ |
| Hypervisor | VMware ESXi **8.0 or later**   |
| Hypervisor | KVM (Red Hat **9.3 or later**) |
| Firmware   | UEFI recommended               |
| Time Sync  | NTP must be enabled            |

## Minimum System Requirements

**Note** : These values are for evaluation or lab use only and are not recommended for production.

| Deployment Type          | CPU (Cores) | Memory (RAM) | Disk (SSD) | Supported Devices |
| ------------------------ | ----------- | ------------ | ---------- | ----------------- |
| A10 Control Lite     | 16          | 64 GB        | 700 GB     | 1                 |
| A10 Control Standard | 32          | 128 GB       | 700 GB     | 1                 |

## Deployment Readiness Check

Before starting the installation, make sure the following items are ready:

### Required Files

A10 Control image file (ISO): Download the image from the A10 Networks Support portal.

Deployment Planning

Number of nodes: Decide whether you are deploying a standalone node or a multi-node cluster. For guidance, see System and Sizing Requirements.

Network Configuration Details

Have the following network information available:

Interface IP addresses: IP addresses assigned to each A10 Control interface.

Gateway IP address: Default gateway for the subnet.

Floating IP address: Virtual IP used to access the A10 Control GUI and APIs.

Notes:

IPv6 addressing is supported from ACOS 7_0_1-P1 and later.

SSH access is supported only through the interface IP address. SSH access using the floating IP is not supported.

For standalone deployments with multiple interfaces and for multi-node deployments, GUI access is available through the floating IP of the management interface.

Time and Name Resolution

NTP server IP address: Used for time synchronization.

DNS server IP address: Used for resolving hostnames and application URLs.

Note:
If DNS is not configured, A10 Control cannot resolve the URLs of integrated services such as LDAP, SMTP, and A10 Global License Manager.

Download the A10 Control Image File

Follow these steps to download the A10 Control software image:

Open a supported web browser and go to the A10 Networks Support Portal.

Log in using your A10 Networks account credentials.

Go to Software Downloads and Documentation.

Select the Software tab.

Navigate to the A10 Control section.

Download the required image file:

A10 Control ISO

After the download is complete, verify the file and keep it ready for deployment.
