Zabbix 3.2 Dell Compellent
==========================

This template (Template Dell Compellent) use the COMPELLENT-MIB to discover and manage COMPELLENT Storage Array in Zabbix 3.2.

Original Zabbix 2.x Template is avialable here: [jjmartres/Zabbix](https://github.com/jjmartres/Zabbix/tree/master/zbx-templates/zbx-dell-compellent)

Discovery rules
---------------

* Controller
* Disk
* Enclosure
* Enclosure Fan
* Enclosure Power
* Enclosure Temperature
* Fan
* Power
* Server
* Temperature
* Volume

Installation
------------

1. Import **Template Dell Compellent.xml** file into Zabbix.
2. Add to your host the **{$SNMP_COMMUNITY}** macro with your SNMP community as value.
3. Configure **Host Inventory** to `Automatic` for your host.
4. Associate **Template Dell Compellent** template to the host.

### Requirements

This template was tested for Zabbix 3.2 and higher.
This template was tested for Compellent Storage Center version 6.6.5 and higher.

License
-------

This template is distributed under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the  License, or (at your option) any later version.

### Copyright

  * Copyright (c) Jean-Jacques Martrès
  * Copyright 2015 Andrea Sosso Licensed under the MIT License

### Authors

  * Jean-Jacques Martrès (jjmartres |at| gmail |dot| com)
  * Andrea Sosso @asosso

### Contribute

Contributions are welcome.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
