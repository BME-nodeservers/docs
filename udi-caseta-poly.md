# Lutron Caseta Node Server
Copyright(C) 2022 Robert Paauwe

This node server provides an interface between the [Universal Devices Inc. ISY Controller](https://www.universal-devices.com/residential/ISY)
and [Lutron Caseta (tm)](https://www.casetawireless.com) SmartBridge and connected devices.

Once the SmartBridge is paired to the Lutron Caseta Node Server, devices connected to the SmartBridge
are exposed to the ISY as device nodes.  These devices nodes can then be controlled, integrated into
scenes and programs.

This should support all known Caseta devices. If an unknown device type is encounted, it will log 
information about that device in the log so that the info may be passed on to the developer.

In addition, most Lutron automated shade/blind devices should be supported.  

Current known devices:


PD-5ANS          - switch
PD-6ANS          - switch
PD-5NE           - dimmer switch
PD-6WCL          - dimmer swtich
PD-FSQN          - fan
PD-3PCL          - dimmer module
PD-15OUT         - outdoor plug
PD-OSENS         - occupancy motion sensor
PD-VSENS         - vacancy motion sensor
PJ2-2B-GXX-X01   - Pico 2 button remote
PJ2-2BRL-GXX-X01 - Pico 2 button raise/lower remote
PJ2-3B-GXX-X01   - Pico 3 button remote
PJ2-3BRL-GXX-X01 - Pico 3 button raise/lower remote
PJ2-4B-GXX-X01   - Pico 4 button remote
MACL-LFQH        - maestro fan control and light dimmer (TBD)

Serena shades
QS Wireless Shades
Triathon Shades

