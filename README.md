
check_nexenta
=============

This check plugin for Nagios / Icinga / Icinga2 enables to check a Nexenta fileserver for its health. It queries the 
zpool state and for hardware errors the Sun Faultmanager via SNMP.

    $./check_nexenta
    Mandatory parameter 'host' missing in call to "eval"
    
    check_nexenta [-CHt] [long options...] <some-arg>
    	-H STR --host STR       Nexenta hostname
    	-C STR --community STR  Nexenta hostname
    	-t INT --timeout INT    Timeout
    
    	--help                  print usage message and exit
    
    ./check_nexenta  -H 192.168.1.15 -C public
    NEXENTA CRITICAL - Sun FaultManager: degraded SLOT 17,K1JBTD2D fault.io.disk.slow-io,fault.io.scsi.cmd.disk.dev.rqs.derr


Installation
------------

You need some perl packages for this script to work:

    apt-get install libnet-snmp-perl \
    		libgetopt-long-descriptive-perl \
    		libmonitoring-plugin-perl

