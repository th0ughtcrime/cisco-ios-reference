# Router commands

## Basic configuration
| Action | Command |
|-|-|
| Enter privileged EXEC mode | `Router> enable` |
| Enter configuration mode | `Router# configure terminal` |
| Enter line configuration mode | `Router(config)# line console 0` |
| Set a hostname | `Router(config)# hostname R1` |
| Set a banner message | `Router(config)# banner motd #Authorized access only#` |
| Show the running configuration | `Router(config)# show running-config` |
| Show the startup configuration | `Router(config)# show startup-config` |
| Save any configuration changes to the startup<br>configuration file | `Router(config)# copy running-config startup-config` |
| Undo all configuration changes by loading the<br>startup configuration file | `Router(config)# copy startup-config running-config` |
| Show active services | `Router# show ip ports all` |
| Show active services (before IOS-XE) | `Router# show control-plane host open-ports` |
| Disable the HTTP server | `Router(config)# no ip http server` |

## Security
| Action | Command |
|-|-|
| Secure user EXEC mode | `Router(config)# line console 0`<br>`Router(config-line)# password cisco`<br>`Router(config-line)# login` |
| Secure privileged EXEC mode | `Router(config)# enable secret class` |
| Secure VTY lines | `Router(config)# line vty 0 15`<br>`Router(config-line)# password cisco`<br>`Router(config-line)# login` |
| Encrypt plaintext passwords | `Router(config)# service password-encryption` |
| Start the AutoSecure Configuration | `Router# auto secure` |
| Set the minimum password length to 8 | `Router(config)# security passwords min-length 8` |
| Block VTY logins for 120 seconds after<br>3 failed attempts within 60 seconds | `Router(config)# login block-for 120 attempts 3 within 60` |
| Log out a session after 5 minutes and<br>30 seconds of inactivity | `Router(config)# line vty 0 15`<br>`Router(config-line)# exec-timeout 5 30`|
| Configure SSH and Telnet | `Router(config)# line vty 0 15`<br>|`Router(config-line)# password cisco`<br>`Router(config-line)# transport input ssh telnet` |
| Configure a domain name | `Router(config)# ip domain name cisco.com` |
| Generate an encryption key | `Router(config)# crypto key generate rsa general-keys modulus 1024` |
| Create a local user | `Router(config)# username Bob secret cisco` |
| Create an admin user with privilege 15<br>and password 'secure' | `Router(config)# username admin1 privilege 15 secret secure` |
| Authenticate VTY logins against the local<br>user database | `Router(config)# line vty 0 15`<br>`Router(config-line)# login local` |

## Interfaces
| Action | Command |
|-|-|
| Show concise interface configuration | `Router# show ip interface brief`<br>`Router# show ipv6 interface brief` |
| Show detailed interface configuration | `Router# show ip interface`<br>`Router# show ipv6 interface` |
| Show routing table | `Router# show ip route`<br>`Router# show ipv6 route` |
| Show IPv4 interface statistics | `Router# show interfaces` |
| Show the list of hops to target host | `Router# traceroute 10.1.1.10` |
| Configure a virtual interface | `Router(config)# interface vlan 1`<br>`Router(config-if)# ip address 192.168.1.1 255.255.255.0`<br>`Router(config-if)# no shutdown` |
| Configure an interface | `Router(config)# interface GigabitEthernet 0/0/0`<br>`Router(config-if)# description link to LAN`<br>`Router(config-if)# ip address 192.168.1.1 255.255.255.0`<br>`Router(config-if)# ipv6 address 2001:db8:acad::1/64`<br>`Router(config-if)# ipv6 address fe80::1 link-local`<br>`Router(config-if)# no shutdown` |
| Disable DNS lookup | `Router(config)# no ip domain-lookup` |
| Discover neighboring devices with CDP | `Router# show cdp neighbors` |
| Configure a loopback interface | `Router(config)# interface loopback 0`<br>`Router(config-if)# ip address 10.0.0.1 255.255.255.0` |
