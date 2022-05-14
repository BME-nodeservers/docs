
# Kaiterra

This is a node server to pull AQI data for Kaiterra devices and make it
available to a [Universal Devices ISY994i](https://www.universal-devices.com/residential/ISY)
[Polyglot interface](http://www.universal-devices.com/developers/polyglot/docs/) with 
Polyglot V3 running on a [Polisy](https://www.universal-devices.com/product/polisy/)

(c) 2020,2021,2022 Robert Paauwe

## Installation

1. Backup Your ISY in case of problems!
   * Really, do the backup, please
2. Go to the Polyglot Store in the UI and install.
3. From the Polyglot dashboard, select the Purple Air node server and configure (see configuration options below).
4. Once configured, the Purple Air node server should update the ISY with the proper nodes and begin filling in the node data.
5. Restart the Admin Console so that it can properly display the new node server nodes.

### Node Settings
The settings for this node are:

#### Short Poll
   * How often to poll the Kaiterra API service for current AQI data (in seconds)
#### Long Poll
   * Not used
#### Custom Parameters
	* A list of Kaiterra devices to monitor. For the 'key', enter a name to use to identify the device (under 14 characters, no special characters). For the 'value' enter the Kaiterra sensor UUID.  You an find this on your dashboard
  * An API key that provides authorized access to your devices.  You can generate an API from your dashboard

## Node substitution variables
### Controller node
 * sys.node.[address].ST      (Node sever online)

### Air Quality node
 * sys.node.[address].CLITEMP (current temperature)
 * sys.node.[address].CLIHUM  (current humidity)
 * sys.node.[address].PM25    (current PM 2.5 value)
 * sys.node.[address].PM10    (current PM 1.0 value)
 * sys.node.[address].CO2LVL  (current Co2 Level)
 * sys.node.[address].VOCLVL  (current VOC Level)


## Requirements
1. Polyglot V3.
2. ISY firmware 5.3.x or later

# Release Notes

- 1.0.0 05/14/2022
   - Initial version.
