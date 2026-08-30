## Validated Features
* Jumbo IP/L2 MTU
* IPv4 packet forwarding over native IPv6-only LLA transport
* Single-session (multi-AF) eBGP between spines and leafs
  * Dynamic neighbors using IPv6 NDP/RA
  * Unique leaf ASNs, identical spine ASN
  * IPv4 Unicast AFI/SAFI – advertising system0/VTEP IPs on leafs using IPv6 next hops
  * L2VPN EVPN AFI/SAFI – signaling overlay
* Underlay/overlay BGP routing policies
  * AS path sets, route policies, prefix sets
* Underlay/overlay ECMP sets
  * BGP maximum paths, allow-multiple-as
  * Overlay – MAC/IP aliasing
* BGP fast failover techniques (BFD, rapid route withdrawal, rapid update, etc.)
* IPv4 + IPv6 Symmetric IRB
  * IPv4 DHCP Relay + Option 82
  * IPv6 SLAAC
  * Host routing (/32 or /128) via EVPN Type-2 MAC/IP routes + ARP/ND Snooping
  * IRB prefix routing via EVPN Type 5 routes\
  * Anycast GW (IPv4 + IPv6)
* MAC-VRFs with Layer 2 extension over EVPN
  * Advertisement of ARP/ND extended community
  * Conditional advertisement of ARP/ND route only if corresponding local MAC table entry exists
* IP-VRFs with Layer 3 extension over EVPN
  * EVPN-IFL Type 5 GW-IP advertisement and resolution/ECMP
* Bridged and routed VXLAN interfaces
* Shared services (route leaking via inter-instance policies)
* All-active/single-active Ethernet segments
  * Default (mod-based), preference-based DF election
    * Preference based only – AC-DF/non-revertive capabilities
  * Manual DF designation
  * Standby signaling for single-active (LACP/power-off)
  * EVPN-IFL host (Type 2 MAC/IP) ESI aliasing routes
  * Virtual Ethernet Segments (vES) for IP aliasing
* Layer 2 untagged/Layer 2 tagged/Layer 3 downlink configurations
* Single-homed/multi-homed port configurations
  * Multihoming via LACP/static LAG/active-backup (no LAG)
  * Ethernet reload-delay for all-active configurations
  * LACP fallback mode for LACP LAGs
* PE-CE IPv4/IPv6 unicast eBGP peerings
  * Replace peer AS (AS override)
  * Route redistribution from/to EVPN-IFL (Type 5)
  * Peering to anchor leafs and to directly connected leafs
* Node isolation handling via Event Handler
