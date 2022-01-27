Test connectivity
`C:\> ping 192.168.1.254`

Show networking information
`C:\> netstat`

Show the routing table
`C:\> netstat -r`

Show the list of hops to target host
`C:\> tracert 10.1.1.10`

Show concise IP configuration
`C:\> ipconfig`

Show detailed IP configuration
`C:\> ipconfig /all`

Renew the IP configuration as a DHCP client
`C:\> ipconfig /release`
`C:\> ipconfig /renew`

Do a DNS lookup
`C:\> nslookup www.domain.com`

Show cached DNS information
`C:\> ipconfig /displaydns`

Show cached ARP information
`C:\> arp -a`