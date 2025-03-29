# Meross Plug-in
Copyright(C) 2025 Robert Paauwe

This plug-in integrates Meross (https://www.meross.com) smart home
devices. Meross devices are WiFi based devices that are typically
managed using the Meross mobile App and communicate via a 
proprietary API with the Meross servers.

Since the API is proprietary and not publicly documented, this 
plug-in is based on various efforts to reverse engineer the protocol
and as such, may break if Meross makes changes to the API.

While developing this plug-in I've experienced significant issues
simply getting the devices to work.  It took many attempts to
pair/provision the MSS115 plugs with the mobile app. The SmartHub
continues to go off-line frequently and fails to accept commands 
being sent to it.  At this point, I can't recommend purchasing 
Meross devices based on the existence of this plug-in.

Supported devices:
  MSS115   (Smart plug mini)
  MSH300HK (SmartHub)
  MS200    (SmartHub + door/window sensor)

If you have devices that are not on the above supported device list,
please note that it's typically not a lot of effort to add support 
for other devices.  If you run the plug-in, it will output the
information I need to add support for unknown device types in the
log.  Sending that log to me should provide enough information for 
me to add support for these devices into the plug-in.

TBD support:
  MSL120 (RGB Bulb)
  MSS110 (Smart plug)
  MSS210 (Smart plug)
  MSS305 (Smart plug with power consumption)
  MSS310 (Smart plug with power consumption)
  MSS310h (Smart plug with power consumption)
  MSS425E/MSS425F (Smart strip)
  MSS530H (Wall-mount switches)
  MSG100 (Garage opener)
  MSG200 (3-doors Garage opener)
  MSH300 (Smart hub + valve thermostat)
  MS100 (Smart hub + temperature/humidity sensor)
  MS100F (temperature/humidity sensor)
  MSS710
  MSXH0 (Smart Humidifier)

