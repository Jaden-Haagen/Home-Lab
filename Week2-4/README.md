**CCNA Course Review**  
Learned how switches work, their importance in a network, how to configure a switch, and how to use commands to locate devices and troubleshoot connections.  

**Home Lab Review**  
Installed dnsmasq onto pi and created a new dhcpcd.config file to allow custom configuration and saved the original file as dhcpcd.config.orig as a backup in the event that I mess up the config file. Set the static IP to 10.0.0.3 before deciding to change the structure of the network and add multiple VLANs to separate things.  

Decided to create multiple VLANs for the switch to practice configuring the switch and port assignments. Created 3 vlans Vlan10 on 10.0.10.1/25, Vlan20 on 10.0.20.1/25, and Vlan99 on 10.0.99.2/25. Vlan99 was created specifically for the pi router so I could keep all devices separate in the lab environment. I then updated the port assignments as follows: ports 1 and 2 were assigned to Vlan10, ports 3 and 4 were assigned to Vlan20, and port 24 was assigned to Vlan99. All other ports were disabled to prevent unnecessary and unwanted connections on the switch.  

Had issues where I couldn't route traffic between devices and realised, after troubleshooting by pinging devices and checking each device's network settings, that I had forgotten to manually assign a static IP for the pi, so nothing could talk to it to get an IP address for the network.
