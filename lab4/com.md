vlan 70
vlan 80
vlan 90
vlan 100
vlan 110

int range gig1/0/1-5
switchport mode trunk
exit

ip routing
router ospf 10
network 192.168.102.92 0.0.0.3 area 0
network 195.136.17.12 0.0.0.3 area 0
network 192.168.101.88 0.0.0.3 area 0
network 195.168.102.64 0.0.0.15 area 0
network 192.168.102.94 0.0.0.3 area 0
network 192.168.102.96 0.0.0.3 area 0

ip route 0.0.0.0 0.0.0.0 195.136.17.2
ip route 0.0.0.0 0.0.0.0 195.136.17.6 

interface vlan 70
ip addres 192.168.101.65 255.255.255.192
ip helper-address 192.168.102.67

interface vlan 80
ip addres 192.168.101.129 255.255.255.192
ip helper-address 192.168.102.67

interface vlan 90
ip addres 192.168.101.193 255.255.255.192
ip helper-address 192.168.102.67

interface vlan 100
ip addres 192.168.102.1 255.255.255.192
ip helper-address 192.168.102.67

interface vlan 110
ip addres 192.168.102.65 255.255.255.192
ip helper-address 192.168.102.67
