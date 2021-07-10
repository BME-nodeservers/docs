
# WeatherBit weather service

This is a node server to pull weather data from the WeatherBit weather network and make it available to a [Universal Devices ISY994i](https://www.universal-devices.com/residential/ISY) [Polyglot interface](http://www.universal-devices.com/developers/polyglot/docs/) with  [Polyglot V3](https://github.com/UniversalDevicesInc/pg3)

(c) 2019-2021 Robert Paauwe

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
   * How often to poll the WeatherBit weather service for current condition data. Note that the free plan only updates data hourly. Setting this to less than 3600 seconds may result in exceeding the free service rate limit.
#### Long Poll
   * How often to poll the WeatherBit weather service for forecast data. Note that the free plan only updates data hourly. Setting this to less than 3600 seconds may result in exceeding the free service rate limit.

#### APIkey
	* Your API ID, needed to authorize connection to the WeatherBit API.
#### Elevation 
	* The elevation, in meters, of the location. Default is 0
#### Forecast Days
	* The number of days of forecast data to track (0 - 16)
#### Location 
	* Location to get data for.  Can be specified as:
    - lat&lon      Ex: lat=38.123&lon=-78.543
	- city,state   Ex: city=Raleigh,NC
	- city&contry  Ex: city=Raleigh&country=US
	- city_id      Ex: city_id=8953360
	- station      Ex: station=KSEA
	- postal_code  Ex: postal_code=27601
	- postal_code&country   Ex: postal_code=27601&country=US
#### Plant Type
	* Used as part of the ETo calculation to compensate for different types of ground cover.  Default is 0.23
#### Units    
	* M for si and I for imperial. Default is M

To get an API key, register at www.weatherbit.io

## Node substitution variables
### Current condition node
 * sys.node.[address].ST      (Node sever online)
 * sys.node.[address].CLITEMP (current temperature)
 * sys.node.[address].CLIHUM  (current humidity)
 * sys.node.[address].DEWPT   (current dew point)
 * sys.node.[address].BARPRES (current barometric pressure)
 * sys.node.[address].GV4     (current wind speed)
 * sys.node.[address].WINDDIR (current wind direction )
 * sys.node.[address].GV15    (current visibility)
 * sys.node.[address].SOLRAD  (current solar radiation)
 * sys.node.[address].GV13    (current weather conditions)
 * sys.node.[address].GV14    (current percent cloud coverage)
 * sys.node.[address].RAINRT  (current precipitation rate)
 * sys.node.[address].GV2     (current feels like temperature)
 * sys.node.[address].GV16    (current UV index)
 * sys.node.[address].GV17    (current air quality)

### Forecast node
 * sys.node.[address].CLIHUM  (forecasted humidity)
 * sys.node.[address].BARPRES (forecasted barometric pressure)
 * sys.node.[address].DEWPT   (forecasted dew point)
 * sys.node.[address].RAINRT  (forecasted rain rate)
 * sys.node.[address].GV18    (forecasted chance of precipitation)
 * sys.node.[address].GV19    (day of week forecast is for)
 * sys.node.[address].GV0     (forecasted high temperature)
 * sys.node.[address].GV1     (forecasted low temperature)
 * sys.node.[address].GV13    (forecasted weather conditions)
 * sys.node.[address].GV14    (forecasted percent cloud coverage)
 * sys.node.[address].GV6     (forecasted precipitation accumulation)
 * sys.node.[address].GV7     (forecasted snow accumulation)
 * sys.node.[address].GV8     (forecasted snow depth)
 * sys.node.[address].GV16    (forecasted UV index)
 * sys.node.[address].GV10    (forecasted Ozone)
 * sys.node.[address].GV15    (forecasted Visibility)
 * sys.node.[address].GV9     (forecasted Moon phase)
 * sys.node.[address].GV20    (calculated ETo for the day)


## Requirements

1. A Polisy running Polyglot V3
2. ISY firmware 5.3.x or later
3. An account with OpenWeatherMap (http://www.openweathermap.org)


# Release Notes

- 2.0.0 07/08/2021
   - Ported to Polyglot version 3
- 1.0.8 07/07/2020
   - Convert int to string for display in debug message.
- 1.0.7 06/11/2020
   - Correrct UOM for ETo.
- 1.0.6 04/11/2020
   - Snow depth was incorrectly renamed to rain today, rename it back.
- 1.0.5 04/10/2020
   - Current conditions report rain rate not rain accumulation
- 1.0.4 03/16/2020
   - Change first forecast address to forecast_0 to match other weather node servers.
- 1.0.3 12/31/2019
   - Fix bug when forecast days is set to zero.
- 1.0.2 12/19/2019
   - Fix bug that prevented custom parameter changes from taking immediate
     effect.
- 1.0.1 12/18/2019
   - Use correct UOM (74) for solar radiation
- 1.0.0 12/08/2019
   - Initial version published to github 
