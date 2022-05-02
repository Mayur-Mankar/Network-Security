# Overview
You are required to design and implement Vic Modern Hotel Network. The hotel has three floors; in the first floor there are three departments (Reception, store and Logistics), in the second floor there are three departments (Finance, HR and sales), While the third floor hosts the IT and Admin.
# Policy requirements
The following are part of the considerations during the design and implementation:
*	There should be three routers connecting each floor (all placed in the server room in IT department).
*	All the routers should be connected to each other using serial DCE cable.
*	The network between the routers should  be 10.10.10.0/30, 10.10.10.4/30, 10.10.10.8/30
*	Each floor is expected to have one switch (placed in the respective floor)
*	Each floor is expected to have WIFI networks for connection to laptop and phones
*	Each department is expected to have printer
*	Each department is expected to be in different VLAN with the following details.

1st floor:<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Reception: VLAN 80, Network of 192.168.8.0/24<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Store: VLAN 70, Network of 192.168.7.0/24<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Logistics: VLAN 60, Network of 192.168.6.0/24<br />
2nd floor:<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Finance: VLAN 50, Network of 192.168.5.0/24<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;HR: VLAN 40, Network of 192.168.4.0/24<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sales: VLAN 30, Network of 192.168.3.0/24<br />
3rd floor:<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Admin: VLAN 20, Network of 192.168.2.0/24<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;IT: VLAN 10, Network of 192.168.1.0/24<br />
*	Use OSPF as the routing protocol to advertise routes
*	All devices in the network are expected to obtain IP address dynamically with their respective router configured as the DHCP server.
*	All the devices in the network are expected to communicate with each other.
*	Configure SSH in all the routers for remote login.
*	In IT department, add PC called Test-PC to port Fa0/1 and use it to test remote login
*	configure port security on IT-department switch to allow only Test-PC to access the port Fa0/1 (use sticky mode to learn mac address with violation mode of shutdown)

# Configuration on Switches
The configuration for switches needs separate VLAN for respective department and the Trunk should be configured on the interface connected with the router.
# Configuration on Routers
The configuration for router needs configuration of sub-interfaces, DHCP, static IP addresses.
