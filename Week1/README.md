# Week 1 - Network Basics and Lab Setup  

Learned what the basic devices are and their jobs (switches, routers, cables (ethernet and fiber), etc).  

## Home Lab Set up
Installed Raspberry Pi OS onto an SD card and booted it on the Raspberry Pi. After giving it a minute to boot, I checked the connection from my laptop with SSH. An issue arose with ports 22 and 2222 not accepting connections. Reconnected the SD card to my laptop and added a file named ssh. This allowed SSH after I reconnected the SD card and booted the Pi back up. Then ran updates and rebooted the Pi again.  

Installed Ubuntu iso onto a bootable USB stick, plugged it into the PC, and booted with the USB stick. Installed Ubuntu and, similar to Pi, ran update commands. After updates, I installed Wireshark, nmap, and net-tools. Made sure SSH was enabled and the connection worked by connecting to my laptop and the Pi.  

Set up Tailscale on my laptop, PC, and Pi to ensure I could access home lab devices from my laptop when I wasn't on my home network.  
Installed MobaXterm on my laptop for an easier interface to connect to devices through SSH and RDP. When setting up RDP for the Linux device ran into an issue with the connection not succeeding, and after searching what the issue was determined it was the user not being fully logged out on the device. Resolved by logging back into the device and logging out instead of letting the device hibernate.  

Connected the switch to PC2 with a serial to usb adapter. Used PC2 since Linux has better support for serial connections than Windows. Ran the sudo screen command to pull up the switch interface. Disabled telnet, SNMP, and all ports on initial setup. Set the failsafe account username and password for the switch. Enabled ports 1-4 as an initial test. Updated the admin account password. Saved all changes at this point before logging back in with the admin account. Configured VLAN and added another VLAN before reconfiguring the VLAN to 10.0.0.2 with ip route 10.0.0.1 to avoid any confusion with my home network. After saving I then connected PC 1 and 2 to the switch on ports 1 and 3 and assigned their static ip addresses.  

