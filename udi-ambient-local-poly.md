
# Ambient Weather Station Plug-in for UDI eisy/Polisy

(c) 2018,2021,2025 Robert Paauwe

This is a self-hosted server for receiving weather data directly from the
AmbientWeather console on your local network.  Some AmbientWeather stations
support publishing data to a local server in addition to publishing data
to the Ambient network. This plug-in creates a server that can
receive the data from your local station and re-publish it to an IoX (ISY).

Which weather stations are supported?  

The AmbientWeather documentation does not make this obvious. It has been 
confirmed that the WS-2000 and WS-2902 will, at least with the proper 
firmware.

Configure your Ambient Console for a Custom Server.

1. On your AmbientWeather Console, find where you can configure a custom server
   a. IP Address will the IP Address of your eisy/Polisy
   b. Port will the port number you configured the plug-in to use (defaule 7501)
   c. Path should be: /api/ambientweather/metrics?  ('?' is required)

2. Save your settings

3. Your AmbientWeather Console should now be pushing data to your plug-in

When the plug-in starts, the first data packet it receives is used to configure the plug-in.  It parses the data and builds the necessary nodes to the data provided by your Console.
