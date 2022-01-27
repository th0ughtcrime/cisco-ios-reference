# Basic configuration

Enter privileged EXEC mode
`Switch> enable`

Enter configuration mode
`Switch# configure terminal`

Enter line configuration mode
`Switch(config)# line console 0`

Set a hostname
`Switch(config)# hostname S1`

Set a banner message
`Switch(config)# banner motd #Authorized access only#`

Show the running configuration
`Switch(config)# show running-config`

Show the running configuration
`Switch(config)# show startup-config`

Save any configuration changes to the startup configuration file
`Switch(config)# copy running-config startup-config`

Undo all configuration changes by loading the startup configuration file
`Switch(config)# copy startup-config running-config`

# Security

Secure user EXEC mode
`Switch(config)# line console 0`
`Switch(config-line)# password cisco`
`Switch(config-line)# login`

Secure privileged EXEC mode
`Switch(config)# enable secret class`

Secure VTY lines
`Switch(config)# line vty 0 15`
`Switch(config-line)# password cisco`
`Switch(config-line)# login`

Encrypt plaintext passwords
`Switch(config)# service password-encryption`

Set the minimum password length to 8
`Switch(config)# security passwords min-length 8`

Block VTY logins for 120 seconds after 3 failed attempts within 60 seconds
`Switch(config)# login block-for 120 attempts 3 within 60`

Log out a session after 5 minutes and 30 seconds of inactivity
`Switch(config)# line vty 0 15`
`Switch(config-line)# exec-timeout 5 30`

Configure SSH and Telnet
`Switch(config)# line vty 0 15`
`Switch(config-line)# password cisco`
`Switch(config-line)# transport input ssh telnet`

Configure a domain name
`Switch(config)# ip domain name cisco.com`

Generate an encryption key
`Switch(config)# crypto key generate rsa general-keys modulus 1024`

Create a local user
`Switch(config)# username Bob secret cisco`

Create an admin user with privilege 15 and password 'secure'
`Router(config)# username admin1 privilege 15 secret secure`

Authenticate VTY logins against the local user database
`Switch(config)# line vty 0 15`
`Switch(config-line)# login local`

# Interfaces 

Show concise interface configuration
`Switch# show ip interface brief`

Show detailed interface configuration
`Switch# show ip interface`

Show concise VLAN configuration
`Switch# show vlan brief`

Show detailed VLAN configuration
`Switch# show vlan`

Show IPv4 interface statistics
`Switch# show interfaces`

Show the list of hops to target host
`Router# traceroute 10.1.1.10`

Set the default gateway
`Switch(config)# ip default-gateway 192.168.1.1`

Configure a virtual interface
`Switch(config)# interface vlan 1`
`Switch(config-if)# description link to LAN`
`Switch(config-if)# ip address 192.168.1.2 255.255.255.0`
`Switch(config-if)# no shutdown`

Disable DNS lookup
`Switch(config)# no ip domain-lookup`

Discover neighboring devices with CDP
`Switch# show cdp neighbors`

Create and name a VLAN
`Switch(config)# vlan 20`
`Switch(config-vlan)# name student`

Show switch port information
`Switch# show interfaces fa0/18 switchport`

Assign a switch port to a VLAN
`Switch# configure terminal`
`Switch(config)# interface fa0/6`
`Switch(config-if)# switchport mode access`
`Switch(config-if)# switchport access vlan 20`