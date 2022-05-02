# Overview
We are required to design and implement the communication between three sites A, B and C. and site-to-site IPsec tunnel communication between site-B and site-C for all ip traffic.

# Policy Requirements
The following are part of the considerations during the design and implementation.
* There should be three routers connecting each sites A, B and C respectively
*	All the routers should be connected to each other using serial DCE cable.
*	The network between the routers should be 10.10.1.0/30,10.10.1.4/30,10.10.1.8/30
*	Each site is expected to have one switch and server
*	Site-C is expected to have one PC including the server 
*	Site-B and C server connected with switch is expected to be in separate VLAN with the following details.
Site-B: Server-B: VLAN 20, Network of 192.168.2.0/24
Site-C: Server-C: VLAN 20, Network of 192.168.3.0/24
*	Use OSPF as the routing protocol to advertise routes
*	Configure port security on each switch to allow only respective end device to access the port use sticky mode to learn mac address with violation mode of shutdown
*	On the router for Site A 2911 (Site A will be directly connected to Site B and C) 
*	Allow only http traffic from site B and C to the Webserver in the site A
*	Allow ip traffic from site B to site C and from site C to site B
*	Configure a site-to-site VPN between Site B and Site C using an IPsec encrypted tunnel. You will use pre-shared keys for authentication to initialize the VPN. You will allow http traffic across the tunnel.
*	Configure Dynamic NAT with PAT (Overloading) The Server and PC IP addresses will be translated.
# Configuration on Switches
The configuration for switches needs separate VLAN for Server and the Trunk should be configured on the interface connected with the router.
# Configuration on Routers
The configuration for router needs configuration of sub-interfaces, static IP addresses, IPsec vpn, ACL.
