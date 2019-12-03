SW
enable 
conf t
username marcelocardinal privilege 15 secret vamosficarquietos
username leonardomelo privilege 15 secret leozin
vlan 779
interface f0/1
switchport mode access 
switchport access vlan 779
interface f0/2 
switchport mode access
switchport access vlan 780
interface g0/1
switchport mode trunk 
switchport trunk native vlan 999
switchport trunk allowed vlan 779,780,999


RT

enable 
conf t 
interface g0/0.779
encapsulation dot1q 779 
ip address 172.16.0.1 255.255.255.0
ip helper-address 172.16.10.62
interface g0/0.780
encapsulation dot1q 780
ip address 172.16.10.1 255.255.255.0
interface serial0/3/0 
ip address 187.13.243.2 255.255.255.252
