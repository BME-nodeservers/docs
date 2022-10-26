
# Davis Weatherlink polyglot

This is the Davis WeatherLink Poly for the [Universal Devices ISY994i](https://www.universal-devices.com/residential/ISY) [Polyglot interface](http://www.universal-devices.com/developers/polyglot/docs/) with  [Polyglot V3](https://github.com/UniversalDevicesInc/pg3)

(c) 2020,2021 Robert Paauwe

This node server is intended to support [Davis Weather Stations](http://www.davisinstruments.com/).  This is for use with the WeatherLinkIP, the Serial/USB Data Logger with the WeatherLink Computer Software, or the Vantage Connect weather station solutions.  [API documentation](https://www.weatherlink.com/static/docs/APIdocumentation.pdf). 

## Installation

1. Backup Your ISY in case of problems!
   * Really, do the backup, please
2. Go to the Polyglot Store in the UI and click Install. You will be redirected to the UDI store to purchase a license for this node server.
3. After purchasing the node server, refresh the store listing.
4. Click the Install button again.
5. After the install completes, go to the dashboard and select OpenWeatherMap 'Details'
6. Configure the node server per configuration section below.

### Node Settings
The settings for this node are:

#### Short Poll
   * How often to poll the Davis server
#### Long Poll
   * Sends a heartbeat as DON/DOF
#### Token
   * Your token that allows access to the data at api.weatherlink.com
#### Device ID
   * Your device id (mac address without colons) that allows access to the data at api.wetherlink.com
#### Password
   * Your password that allows access to the data at api.wetherlink.com
#### Units
   * Display data in either 'metric', 'us' units. Note that day, month, year observations are only available in 'us' units per documentation.
#### Station
   * The Davis station ID. Not currently used.

## Node substitution variables
### Current condition node
 * sys.node.[address].ST      (Node server online)
 * sys.node.[address].CLITEM  (temperature)
 * sys.node.[address].CLIHUM  (humidity)
 * sys.node.[address].DEWPT   (dewpoint)
 * sys.node.[address].GV3     (heat index)
 * sys.node.[address].GV4     (windchill)
 * sys.node.[address].BARPRES (pressure)
 * sys.node.[address].WINDDIR (wind dir)
 * sys.node.[address].SPEED   (wind speed)
 * sys.node.[address].GV16    (pressure trend)
 * sys.node.[address].SOLRAD  (solar radiation)

### Daily
 * sys.node.[address].GV0     (temp high)
 * sys.node.[address].GV1     (temp low)
 * sys.node.[address].GV2     (dewpt high)
 * sys.node.[address].GV3     (dewpt low)
 * sys.node.[address].GV4     (heatidx high)
 * sys.node.[address].GV5     (windchill low)
 * sys.node.[address].GV8     (humidity high)
 * sys.node.[address].GV9     (humidity low)
 * sys.node.[address].GV10    (pressure high)
 * sys.node.[address].GV11    (pressure low)
 * sys.node.[address].GV12    (preciptitation)
 * sys.node.[address].RAINRT  (rain rate)
 * sys.node.[address].SPEED   (wind speed)
 * sys.node.[address].GV13    (wind gust)
 * sys.node.[address].SOLRAD  (Solarradiation)
 * sys.node.[address].UV      (UV Index)
 * sys.node.[address].GV20    (ETo)

### Monthly
 * sys.node.[address].GV0     (temp high)
 * sys.node.[address].GV1     (temp low)
 * sys.node.[address].GV2     (dewpt high)
 * sys.node.[address].GV3     (dewpt low)
 * sys.node.[address].GV4     (heatidx high)
 * sys.node.[address].GV5     (windchill low)
 * sys.node.[address].GV8     (humidity high)
 * sys.node.[address].GV9     (humidity low)
 * sys.node.[address].GV10    (pressure high)
 * sys.node.[address].GV11    (pressure low)
 * sys.node.[address].GV12    (preciptitation)
 * sys.node.[address].RAINRT  (rain rate)
 * sys.node.[address].SPEED   (wind speed)
 * sys.node.[address].SOLRAD  (Solarradiation)
 * sys.node.[address].UV      (UV Index)
 * sys.node.[address].GV20    (ETo)

### Yearly
 * sys.node.[address].GV0     (temp high)
 * sys.node.[address].GV1     (temp low)
 * sys.node.[address].GV2     (dewpt high)
 * sys.node.[address].GV3     (dewpt low)
 * sys.node.[address].GV4     (heatidx high)
 * sys.node.[address].GV5     (windchill low)
 * sys.node.[address].GV8     (humidity high)
 * sys.node.[address].GV9     (humidity low)
 * sys.node.[address].GV10    (pressure high)
 * sys.node.[address].GV11    (pressure low)
 * sys.node.[address].GV12    (preciptitation)
 * sys.node.[address].RAINRT  (rain rate)
 * sys.node.[address].SPEED   (wind speed)
 * sys.node.[address].SOLRAD  (Solarradiation)
 * sys.node.[address].UV      (UV Index)
 * sys.node.[address].GV20    (ETo)


## Requirements

1. A Polisy running Polyglot V3
2. ISY firmware 5.3.x or later
3. A Davis weatherstation and WeatherLink account

# Release Notes

  2.0.0 07/.12/2021
   - Port to Polyglot version 3
- 1.0.5 08/17/2020
   - Don't use the request results in the error message when request fails
- 1.0.4 08/04/2020
   - Changed "User" to "Device ID" as that represents what configuration is really needed.
- 1.0.3 07/05/2020
   - Remove call to set_hub_timestamp since it doesn't exist and causes error.
- 1.0.2 04/05/2020
   - Add a bunch of error checking.
- 1.0.1 04/05/2020
   - Add some additional error reporting to query failures.
- 1.0.0 04/04/2020
   - Initial version published to github
