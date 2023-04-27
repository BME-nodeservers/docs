
# NOYITO - 2 channel USB relay board.

A node server that works with the Noyito USB relay boards.  Currently
only the 2 channel board is supported.

This make work with other brands of USB relay boards if they use the
same protocol.

The Noyito board is availble from Amazon at:
[https://www.amazon.com/NOYITO-2-Channel-Module-Control-Intelligent/dp/B081RM7PMY]

# Configuration
The node server will poll the board at the short poll interval for any changes in
the relay states.

To configure the node server, you need to specify the serial device created
when the board is connected.  The device should be one of the /dev/ttyUx devices.

When used with PG3, you may have to set the permissions of the device so that 
polyglot can access it. Doing

sudo chmod 666 /dev/ttyUx

subsituting the actual device name for the ttyUx above.

PG3x should take care of setting the correct permissions for you.

