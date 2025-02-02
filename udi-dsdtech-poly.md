
# DSD Tech - SH-UR01A USB relay board.

A node server that works with the DSD Tech USB relay board.

This may work with other brands of USB relay boards if they use the
same protocol.

The DSD Tech board is availble from Amazon at:
[https://www.amazon.com/dp/B09PYML6Q7?psc=1&ref=ppx_yo2ov_dt_b_product_details]

# Configuration
The node server will poll the board at the short poll interval for any changes in
the relay states.

To configure the node server, you need to specify the serial device created
when the board is connected.  The device should be one of the /dev/ttyUx devices.

# PG3 only configuration
When used with PG3, you may have to set the permissions of the device so that 
polyglot can access it. Doing

sudo chmod 666 /dev/ttyUx

subsituting the actual device name for the ttyUx above.

Alternatly, you can configure it to automatically set the owner/permissions of the device
when it is plugged in by copying:

attach 100 {
	match "vendor" "0x10c4";
	match "product" "0xea60";
	action "chown polyglot /dev/tty$ttyname";
	action "chmod 0600 /dev/tty$ttyname";
};

to /etc/devd/dsdtech.conf and restarting devd (service devd restart)


# PG3x only configuration
PG3x should create the config file and restart devd automatically on node server install.

