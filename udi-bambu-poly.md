
# Bambu Lab Plug-in
(c) 2025 Robert Paauwe

A [Universal Devices, Inc.](https://www.universal-devices.com/residential/ISY)
PG3x plug-in to enable support for the [Bambu Lab](https://www.bambulab.com)
line of 3D printers.

This plug-in is designed primarily to monitor the 3D printers but is able to 
control some features such as nozzle/bed temperatures and pause/resume/stop.

When the plug-in starts, it makes a connection to the printer and from that
point on, the printer will continuously send updates of it's status to the
plug-in.

The plug-in monitors:
* Printer State - current operating state of the printer
* Bed target temperature - temperature set that the printer is trying to maintain
* Bed current temperature - the current temperature of the bed
* Nozzle target temperature - temperature set that the printer is trying to maintain
* Nozzle current temperature - the current temperature of the nozzle
* Cooling fan speed - the current part cooling fan speed
* Chamber light - chamber light on/off
* Printer speed - current set printer speed
* Layer number - the layer number that is currently being printed
* Time Remaining - How many minutes are estimated until the print is done
* File name - the name of file being printed
* Gcode state - what state the printer is in during the processing of gcode
* Percent done - what percentage of the print is done

The plug-in can control:
* Print speed
* Chamber light
* Fan speed
* Bed temperature
* Nozzle temperature
* Pause printing
* Resume printing
* Stop/quit printing

The plug-in also creates nodes for the external spool and any attached AMS
units.  These node simply display some basic information about the filament
loaded on the various spools (or trays as Bambu Lab calls them). The most
useful is probably the filament type and color.  The rest of the information
seems to only be available from the AMS and not the AMSLite units.

This plug-in uses the LAN network mode on the printers for communication.
This means that you need to authorize the plug-in to connect to the 
printer with the IP address, Access Code, and printer serial number.

### Plug-in Configuration

#### Short Poll
   * Not used
#### Long Poll
   * Not used

Use the "Add Printer" button to add a printer configuration and enter:
#### Printer Name 
   * What you want to call the printer, this is used as the node name so must follow UDI node naming conventions.
#### IP Address
   * The IP Address of the printer
#### Access Code
   * The access code listed in the printer settings->LAN only mode
#### Serial Number
   * The printer serial number list in settings->device->printer SN


# Should you have an issue
This plug-in was developed and tested using Bambu Lab's A1 with an
AMSLite and a A1 Mini.  While it should work for any Bambu Lab printer
mode, has not be tested with X1 or P series printers nor with AMS units.

If you encounter issues running this plug-in please use the following
steps to help resolve the issue.

1) Switch the plug-in's logging level to debug
2) Restart the plug-in
3) After you've verified the issue is still happening, download the plug-in's log package.
4) Send me a PM on UDI forums, describe the issue you are having and attach the log package you downloaded.

Having this log package is the only way I am able to see what is happening
when you are running the plug-in.
