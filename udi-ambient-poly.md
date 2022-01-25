
# AmbientWeather-polyglot

This is the Ambient Weather Poly for various [Ambient Weather stations] (https://www.ambientweather.com/) [Polyglot interface](http://www.universal-devices.com/developers/polyglot/docs/) with Polyglot V3 running on a [Polisy](https://www.universal-devices.com/product/polisy/)

(c) 2018,2021 Robert Paauwe

This node server is intended to support the [Ambient Weather Station](http://www.ambientweather.com/). 

## Installation

1. Backup Your ISY in case of problems!
   * Really, do the backup, please
2. Go to the Polyglot Store in the UI and install.
3. From the Polyglot dashboard, select the Ambient Weather node server and configure (see configuration options below).
4. Once configured, the Ambient Weather node server should update the ISY with the proper nodes and begin filling in the node data.
5. Restart the Admin Console so that it can properly display the new node server nodes.

### Node Settings
The settings for this node are:

#### Short Poll
   * How often to poll the Ambient Weather servers for data (in seconds)
#### Long Poll
   * Not used
#### API Key (key = APIKey)
   * Your Ambient Weather account API Key. This authorizes the node server to access your weather data.


## Requirements
1. Polyglot V3.
2. ISY firmware 5.3.x or later.
3. An Ambient Weather station and account.

# Release Notes

- 2.0.4 1/24/2022
   - Fix nls mapping for rain values.  
   - Don't look at eventrain, use hourlyrain instead for rain rate.
   - Change battery UOM, it's not voltage but just a ok/low indication.
   - Fix bug in stop. It was calling the old name to set the station state.
- 2.0.3 1/18/2022
   - Fix co2 battery, move rain to sensor 'main'.
- 2.0.2 1/13/2022
   - Support new field names that don't match the naming convention
- 2.0.1 8/7/2021
   - Initial release for Polyglot version 3
- 0.1.11 9/05/2020
   - Trap error when server sends no data.
- 0.1.10 1/29/2020
   - Trap errors with connecting to Ambient servers.
- 0.1.9 12/27/2019
   - Enable solar radiation reporting if it exists in the data.
- 0.1.8 11/30/2019
   - Check for barometric pressure before trying to calculate trend.
   - Change missing entries from error to warning.
- 0.1.7 11/29/2019
   - Add configurable indoor sensor node
   - Stop forcing all values to be sent every time.
- 0.1.6 11/26/2019
   - Clean up profile files.
- 0.1.5 10/25/2019
   - Improve custom parameter handling for cloud.
- 0.1.4 10/24/2019
   - Improve notices and custom parameter handling.
- 0.1.3 10/21/2019
   - Use correct module import for polyglot cloud.
- 0.1.2 03/20/2019
   - Fix online status going false after query.
- 0.1.1 09/14/2018
   - Fix URL path
- 0.1.0 09/12/2018
   - Initial version published in the Polyglot node server store
