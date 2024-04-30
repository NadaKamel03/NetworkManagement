# Network Implemented with 4 VLANs
This document describes a network design utilizing four VLANs (Virtual Local Area Networks) to segment traffic and enhance security.

# Router

The router will provide the devices in the network with IP addresses through the use of DHCP

# Switch 

The switch will manage all the network traffic and avoid collision between the devices on the network and will allow for connectivity across VLANs (Inter-VLAN connectivity)

# VLAN Breakdown
VLAN 1: Voice (192.168.80.0/24 - Example)

Devices:
IP Phone 1
Description: This VLAN carries Voice over IP (VoIP) traffic for clear and efficient communication. Separating voice traffic reduces congestion on the network and prioritizes call quality.
VLAN 2: Data (192.168.81.0/24 - Example)

Devices:
PC- Workstation
IP Phone 2
Description: This VLAN carries standard data traffic for workstations and allows IP Phone 2 to communicate within the network. This separation keeps general network traffic isolated from voice traffic, potentially improving overall network performance.
VLAN 3: Management (192.168.82.0/24 - Example)

Devices:
Mikrotik 960 (Router)
PC- Workstation
Description: This VLAN is dedicated to network management tasks. The Mikrotik 960, acting as a powerful router, manages inter-VLAN routing and provides network access to workstations in all VLANs. Separating management traffic allows for secure network administration without impacting other functions.
VLAN 4: Security (192.168.83.0/24 - Example)

Devices:
Webcam
Description: This VLAN carries video traffic from the security camera. Isolating security footage enhances network security and potentially improves video stream quality.

# Inter-VLAN Communication:

While each VLAN functions as a separate broadcast domain, communication between VLANs can be achieved through the switch and the Mikrotik 960. This allows, for example, IP phones in VLAN 1 to communicate with workstations in VLAN 2 through properly configured routing rules.

# Benefits of VLAN Implementation:

Improved Security: Separating traffic types minimizes the attack surface and potential for unauthorized access across the network.
Enhanced Performance: Isolating traffic reduces network congestion, leading to smoother performance for voice calls, data transfer, and video streaming.
Simplified Management: Grouping similar devices within a VLAN allows for easier administration and troubleshooting.
