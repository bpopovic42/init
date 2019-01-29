Iconfig output analysis
=======================

## Ifconfig output
``` shell
en0: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	options=10b<RXCSUM,TXCSUM,VLAN_HWTAGGING,AV>
	ether 10:dd:b1:b8:cb:5a
	inet6 fe80::1c0a:872:7776:9b8b%en0 prefixlen 64 secured scopeid 0x4
	inet 10.13.2.14 netmask 0xffff0000 broadcast 10.13.255.255
	nd6 options=201<PERFORMNUD,DAD>
	media: autoselect (1000baseT <full-duplex>)
	status: active
```
|FIELD				|	DETAILS																											|
|-------------------|-------------------------------------------------------------------------------------------------------------------|
|en0				|	Interface name																									|
|flags=8863			|	Number of flags ? : 8863																						|
|UP					|	Indicates that kernel modules related to Ethernet interface has been loaded										|
|BROADCAST			|	Denotes that the Ethernet device supports broadcasting (Necessary for DHCP)										|
|SMART				|	Deprecated flag																									|
|RUNNING			|	Interface is ready to accept data																				|
|SIMPLEX			|	Interface is configured for simplex operations																	|
|MULTICAST			|	Indicates that the Ethernet interface supports multicasting														|
|mtu 1500			|	Short for 'Maximum Transmission Unit', default is 1500															|
|RXCSUM				|	Checksum used to verify data and detect transmission errors on the receiving end								|
|TXCSUM				|	Same as above but for transmitting instead of receiving															|
|VLAN_HWTAGGING		|	See man																											|
|AV					|	See man																											|
|ether				|	NIC's mac address (another name for lladdr or link local address												|
|inet6				|	IPV6 link-local address (see self assigned (fe80) likely means that router isn't configured for ipv6			|
|prefixlen 64		|	Means that 64 bits are reserved for subnetting																	|
|scope id 0x4		|	Scope value for Multicast (See wikipedia ipv6's page)															|
|inet				|	IPV4 local network address																						|
|netmask			|	self-explanatory																								|
|broadcast			|	IPV4 broadcast address																							|
|nd6				|	Neighbor discovery protocol																						|
|PERFORMNUD			|	NUD short for 'Network Unreachability Detection' determines that a neighbor is no longer reachable on the link	|
|DAD				|	? See man																										|

## LINKS:
[Useful iPython book](https://gist.github.com/arntzy/425b893e0284803fe140) ([Can be read here](https://nbviewer.jupyter.org/gist/arntzy/425b893e0284803fe140))
[Wikipedia page on link-local addresses](https://en.wikipedia.org/wiki/Link-local_address)
[Wikipedia page on IPV6 address scopes](https://www.wikipedia.com/en/IPv6_address#/IPv6_address_scopes/)
