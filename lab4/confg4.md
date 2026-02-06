Enterprise Networking Project #7
Melbourne Health Services is a well-established health provider in Australia, which offers
health solutions and services to its clients. The institution operates in two locations within the
same city, having the hospital headquarters 20km away from the branch hospital. Therefore,
it has the following departments within its main headquarters Medical Lead Operation &
Consultancy Services (MLOCS), Medical Emergency and Reporting (MER), Medical
Records Management (MRM), Information Technology (IT), and Customer Service (CS).
The branch hospital was designed to share the workloads with the headquarters hence it
contains the following departments; Nurses & Surgery Operations (NSO), Hospital Labs
(HL), Human resource (HR), Marketing (MK), and Finance (FIN). Each location is also
expected to have a Guest/Waiting area (GWA) for patients or visitors.
So far the network was using third-party services to maintain its IT services. The senior
management has decided to own their network infrastructure including Local Area Network
(LAN), Wide Area Network (WAN), and a Server-Side site that is expected to be located
separately at the headquarters and is connected to the HQ Router with an access switch. The
server-side site will host the DHCP server, DNS Server, Web Server, and Email Server.
The network is expected to be cost-effective and observes the information security rule of the
CIA (Confidentiality, Integrity, and Availability). The network is expected to have a
hierarchical model with two already purchased Core routers (one at HQ and one Branch) each
connecting to two subscribed ISPs. Due to security requirements, it has been decided that all
the departments will be on a separate network segment within the same local area network.
You have been hired as a network security engineer to design the network according to the
requirements set by the senior management. You will consult an appropriate robust network
design model to meet the design requirements. You will also implement Access Control Lists
and Virtual Private Network (VPN) to enable secure communication considering security and
network performance factors paramount to safeguarding Confidentiality, Integrity, and
Availability of data and communication. The network security policy will comprehensively
dictate the user's access to each site using Access Control List (ACL).

Network Design and Implementation Requirements
1. Use Cisco Packet Tracer to design and implement the network solution.
2. Use a hierarchical model providing redundancy in the network.
3. Both HQ and Branch routers are expected to be connected using a serial connection.
4. As mentioned earlier, for network cost-effectiveness, each site is expected to have one
core router, two multilayer switches, and several access switches connecting each
department.
5. Each department is required to have a wireless network for the users.
6. Every department in HQ is estimated to have around 60 users while in Branch is
estimated to be 30 users.
7. Each department should be in a different VLAN and a different subnetwork.
8. Provided a base network of 192.168.100.0, and carry out subnetting to allocate the
correct number of IP addresses to each department.
9. The company network is connected to the static, public IP addresses (Internet
Protocol) 195.136.17.0/30, 195.136.17.4/30, 195.136.17.8/30, and 195.136.17.12/30
connected to the two Internet providers.
10. Configure basic device settings such as hostnames, console password, enable password.
banner messaces. and disable IP domain lookun.
11. Devices in all the departments are required to communicate with each other with the
respective multilayer switch configured for inter-VLAN routing.
12. The Multilayer switches are expected to carry out both routing and switching
functionalities and thus will be assigned IP addresses.
13. All devices in the network are expected to obtain an IP address dynamically from the
dedicated DHCP servers located in the server room.
14. Devices in the server room are to be allocated IP addresses statically.
15. Use OSPF as the routing protocol to advertise routes both on the routers and multilayer
switches.
16. Configure default static routing to enable routers and multilayer switches to forward any
traffic that does not match routing table entries. Use next-hop IP addresses.
17. Configure SSH in all the routers and layer three switches for remote login.
18. Configure port-security for the server site department switch to allow only one
device to connect to a switch port, use sticky method to obtain mac-address and
violation mode shutdown.
19. Configure the extended ACL rule together with site-to-site VPN (IPSec VPN) to
create a tunnel and encrypt communication between HQ and the Branch network.
20. Configure PAT to use the respective outbound router interface IPv4 address, and
implement the necessary ACL rule.
21, Test Co/sozication, ensure everything configured is working as expected.
Subt

conf ssh de sw l3
control remoto de sw
conf de routers (falta)
falta conf de sw l3 
conf de routers 
conf de servidores
etc...


############ CONFIG STEPS ###############
0. Netwok Design and beatufication.
1. Basic settings to all devices plus ssh on the routers and 13 switches.
2. VLANs assignment plus all access and trunk ports on 12 and 13 switches.
Switchport security to server-side site department.
4. Subnetting and IP addressing
5. OSPF on the routers and 13 switches.
6. Static IP address to serverRoom devices.
7. DHCP server device configuratiuons.
8. Inter-VLAN routing on the 13 switches plus ip dhcp helper addresses.
9. Wireless network configurations.
10. Site-to-site IPSec VPN
11. Default static route
12. PAT + Access Control List
14. Verifying and testing configurations.




