# Overview
In this project I have designed and implemented a network for company A using ASA 5520 firewall and Edge router. 
Firewall has 4 named networks with defined security levels connected to it. The management network is implemented
through which we can manage edge router, ASA firewall, INSIDE, DMZ and OUTSIDE switch. The inside network can 
access the OUTSIDE and DMZ network, from OUTSIDE network the PC with AnyConnect VPN can securely access the INSIDE 
network using VPN-Tunnel and from OUTSIDE network the DMZ is accessible.
