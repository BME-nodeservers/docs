
# Davis WeatherLink Live

This is a node server to pull weather data from a Davis WeatherLink devicd and make it available to a [Universal Devices ISY994i](https://www.universal-devices.com/residential/ISY) [Polyglot interface](http://www.universal-devices.com/developers/polyglot/docs/) with  [Polyglot V3](https://github.com/UniversalDevicesInc/pg3)

(c) 2019,2021 Robert Paauwe

## Installation

1. Backup Your ISY in case of problems!
   * Really, do the backup, please
2. Go to the Polyglot Store in the UI and click Install. You will be redirected to the UDI store to purchase a license for this node server.
3. After purchasing the node server, refresh the store listing.
4. Click the Install button again.
5. After the install completes, go to the dashboard and select WeatherLinkLive 'Details'
6. Configure the node server per configuration section below.


### Node Settings
The settings for this node are:

#### Short Poll
   * How often the node server will poll the WeatherLink device for current condition data.  This can be a often as every 10 seconds but that may overwhelm the ISY.

#### Long Poll
   * Not used

## Node substitution variables
### Current condition node
 * sys.node.[address].ST      (Node sever online)
 * sys.node.[address].CLITEMP (current temperature)
 * sys.node.[address].CLIHUM  (current humidity)
 * sys.node.[address].DEWPT   (current dew point)
 * sys.node.[address].BARPRES (current barometric pressure)
 * sys.node.[address].SPEED   (current wind speed)
 * sys.node.[address].WINDDIR (current wind direction )
 * sys.node.[address].GV9     (current wind gust speed)
 * sys.node.[address].SOLRAD  (current solar radiation)
 * sys.node.[address].RAINRT  (current precipitation rate)
 * sys.node.[address].GV0     (current wet bulb)
 * sys.node.[address].GV1     (current heat index)
 * sys.node.[address].GV2     (current windchill)
 * sys.node.[address].GV5     (current rain size)
 * sys.node.[address].GV7     (current UV index)
 * sys.node.[address].GV8     (current pressure trend)
 * sys.node.[address].GV10    (current daily rainfall)
 * sys.node.[address].GV11    (current indoor temp)
 * sys.node.[address].GV12    (current indoor humidity)

### Indoor sensor (optional)
 * sys.node.[address].CLITEMP (current temperature)
 * sys.node.[address].CLIHUM  (current humidity)
 * sys.node.[address].DEWPT   (current dew point)
 * sys.node.[address].GV0     (current heat index)

### Soil sensor (optional)
 * sys.node.[address].GV0     (current soil temp 1)
 * sys.node.[address].GV1     (current soil temp 2)
 * sys.node.[address].GV2     (current soil temp 3)
 * sys.node.[address].GV3     (current soil temp 4)
 * sys.node.[address].GV4     (current soil moisture 1)
 * sys.node.[address].GV5     (current soil moisture 2)
 * sys.node.[address].GV6     (current soil moisture 3)
 * sys.node.[address].GV7     (current soil moisture 4)
 * sys.node.[address].GV8     (current wet leaf 1)
 * sys.node.[address].GV9     (current wet leaf 2)


## Requirements

1. A Polisy running Polyglot V3
2. ISY firmware 5.3.x or later

# Release Notes

- 2.0.3 01/23/2022
   - Pass interface instance to new nodes.
- 2.0.2 01/17/2022
   - Check that node exist before updating (soil, indoor)
   - Create indoor node if data type 4 exists, not type 1
- 2.0.1 01/10/2022
   - Fix bug indoor/soil node access
- 2.0.0 07/19/2021
   - Converted to work with Polyglot version 3
- 1.0.6 05/21/2020
   - Remove debug message for exception as ConnectionError exception doesn't
     have a .msg object
- 1.0.5 05/08/2020
   - trap errors when making request to WLL.
- 1.0.4 04/02/2020
   - check for sealevel pressure before trying to use it.
- 1.0.3 08/14/2019
   - Use rain size to calculate rainfall.
   - Replace rain size value with yearly rainfall
- 1.0.2 08/04/2019
   - Add indoor and soil condition nodes
- 1.0.0 07/24/2019
   - Start of development
