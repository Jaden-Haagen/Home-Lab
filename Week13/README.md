Configured access lists  
Had an issue where 10.0.18.2 couldn't ping 10.0.16.4 when testing access list. Used packet tracer simulation mode to watch packet travel network from both sides. Determined it was failing at the connection between routers so looked at configuration for cafe01-RT01 and FO-RT01.  
Found issue when I ran show ip ospf neighbor. State was EXSTART so I reconfigured the routers to have router id 1.1.1.1 and 2.2.2.2, then ran clear ip ospf process on both routers to fix the process
