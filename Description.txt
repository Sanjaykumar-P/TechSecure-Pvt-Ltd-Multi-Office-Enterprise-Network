In this project, I designed the topology for the fictional company **TechSecure Pvt Ltd**. I implemented two offices on different floors, where the two internal networks are connected to a main edge router using **OSPF and default route configurations**.

In both internal networks, I configured **VLAN 10, VLAN 20, and VLAN 30** for different departments such as **HR, Sales, and Finance**. I also enabled **trunking** between the required devices. After that, I configured **Inter-VLAN Routing** on the router so that devices in each VLAN could communicate with each other.

Similarly, for the other internal network, I configured **VLAN 100, VLAN 200, and VLAN 300** and implemented Inter-VLAN Routing. The gateway IP addresses configured for these VLANs included **192.168.100.1, 192.168.200.1, and 192.168.210.1**.

After completing the VLAN and Inter-VLAN Routing configurations, I moved to the routing portion of the project and configured the required routes. At this stage, my devices were able to communicate with the internal networks, but they were not able to communicate with the external network.

To simulate the external network, I created an **ISP router** with **8.8.8.8** as the external destination and configured it accordingly. I also configured a **loopback IP address** on the ISP router.

Initially, when I tried to ping **8.8.8.8** from my internal devices, the ping was not successful because there was no route toward the external network. To resolve this, I configured a **static default route** and then configured **OSPF default-information originate** to advertise the default route into the internal OSPF network.

After these configurations, my internal devices were able to reach the external **8.8.8.8** destination successfully. Finally, I performed end-to-end connectivity testing to verify communication between the internal networks and the external network.
