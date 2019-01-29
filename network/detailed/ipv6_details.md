IPV6 details
============

## Address deconstruction

As in IPv4 addresses, IPv6 addresses are splitted into two components: a network component and a node component.

This was done initially using Address Classes and later using Subnet Masking.

The IPv6 address is split into two 64 bits segments, the top 64 bits is the network part and the lower 64 bits the node part

The upper 64 bits are used for routing.

The lower 64 bits identify the address of the interface or node, and is derived from the actual physical or MAC address using IEEE’s Extended Unique Identifier (EUI-64) format. See this Wiki description for exact details.

If we look at the upper 64 bits in more detail we can see that it is split into 2 blocks of 48 and 16 bits respectively the lower 16 bits are used for subnets on an internal networks, and are controlled by a network administrator.

The upper 48 bits are used for the global network addresses and are for routing over the internet.

![](resources/ipv6-address-structure.jpg)

## Address Types and Scope

IPv6 addresses have three types:
* **Global Unicast Address** - Scope Internet - routed on Internet
* **Unique Local** - Scope Internal Network or VPN internally routable, but **Not routed** on Internet
* **Link Local** - Scope network link - **Not Routed** internally or externally

![](resources/ipv6-address-types.jpg)
