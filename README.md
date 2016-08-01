Zabbix 3.0 Dell Compellent
==========================

This template (ZBX3-DELL-COMPELLENT) use the COMPELLENT-MIB to discover and manage COMPELLENT Storage Array in Zabbix 3.0.

Original Zabbix 2.x Template is avialable here: [jjmartres/Zabbix](https://github.com/jjmartres/Zabbix/tree/master/zbx-templates/zbx-dell-compellent)

Items
-----

  * Contact (Populates host inventory field **Contact**)
  * Device location (Populates host inventory field **Location**)
  * Device manufacturer name (Populates host inventory field **Tag**)
  * Device name (Populates host inventory field **Name**)
  * Device model name (Populates host inventory field **Type**)
  * Device serial number (Populates host inventory field **Serial Number A**)
  * Device software version (Populates host inventory field **OS**)
  * Device management URL (Populates host inventory field **URL A**)
  * Device global status
  * Device reachability using ICMP
  * Device packet loss
  * Uptime
  * Discovery: status for each controller
  * Discovery: Id for each controller
  * Discovery: IP address for each controller
  * Discovery: status for each disk
  * Discovery: status message for each disk
  * Discovery: position for each disk
  * Discovery: status for each enclosure
  * Discovery: status for each volume
  * Discovery: status for each server
  * Discovery: connectivity for each server
  * Discovery: number of path(s) for each server

Triggers
--------

  * **[DISASTER]** => Storage Center is UNREACHABLE or DOWN
  * **[DISASTER]** => Global status of Storage Center is nonrecoverable
  * **[DISASTER]** => Discovery: controller is down
  * **[DISASTER]** => Discovery: disk is down
  * **[DISASTER]** => Discovery: enclosure is down
  * **[DISASTER]** => Discovery: server is down
  * **[DISASTER]** => Discovery: connectivity of server is down
  * **[DISASTER]** => Discovery: volume is down
  * **[HIGH]** => Storage Center has just been restarted
  * **[HIGH]** => Global status of Storage Center is critical
  * **[HIGH]** => Discovery: server has lost path(s)
  * **[AVERAGE]** => Packet loss detected on Storage Center
  * **[AVERAGE]** => Global status of Storage Center is abnormal
  * **[AVERAGE]** => Discovery: controller is degraded
  * **[AVERAGE]** => Discovery: disk is degraded
  * **[AVERAGE]** => Discovery: enclosure is degraded
  * **[AVERAGE]** => Discovery: volume is degraded
  * **[AVERAGE]** => Discovery: server is degraded
  * **[AVERAGE]** => Discovery: connectivity of server is partial
  * **[WARNING]** => Global status of Storage Center is noncritical
  * **[INFORMATION]** => Hostname was changed on Storage Center

Installation
------------

1. Install [`echo.something`](https://github.com/jjmartres/Zabbix/tree/master/zbx-scripts/echo.something) in the **ExternalScripts** directory of your Zabbix server and/or proxy. Check your `zabbix_server.conf` and/or `zabbix_proxy.conf` if in doubt.
2. Then `chmod a+x echo.something`
5. Import **zbx3-dell-compellent.xml** file into Zabbix.
6. Add to your host the **{$SNMP_COMMUNITY}** macro with your SNMP community as value.
7. Configure **Host Inventory** to `Automatic` for your host.
8. Associate **ZBX3-DELL-COMPELLENT** template to the host.

### Requirements

This template was tested for Zabbix 3.0.0 and higher.
This template was tested for Compellent Storage Center version 6.3.10.106 and higher.

###### [echo.something](https://github.com/jjmartres/Zabbix/tree/master/zbx-scripts/echo.something) 1.0

This template use this script to echo "Dell-Compellent Technologies" as Device Manufacturer Name for **Host Inventory**.

License
-------

This template is distributed under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the  License, or (at your option) any later version.

### Copyright

  * Copyright (c) Jean-Jacques Martrès
  * Copyright 2015 Andrea Sosso Licensed under the MIT License

### Authors

  * Jean-Jacques Martrès
  (jjmartres |at| gmail |dot| com)
  * Andrea Sosso @asosso

### Contribute

Contributions are welcome.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
