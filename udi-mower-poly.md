
# Husqvarna automower node server

This is the Husqvarna automower node server for the [Universal Devices ISY994i](https://www.universal-devices.com/residential/ISY) [Polyglot interface](http://www.universal-devices.com/developers/polyglot/docs/) with  [Polyglot V3](https://github.com/UniversalDevicesInc/pg3)

(c) 2018-2021 Robert Paauwe

This node server is intended to interact with Husqvarna Automowers. It can track the mowers status and send commands to control the mower.[Husqvarna](http://www.husqvarnagroup.com/en/automower-435x-awd) You will need account access to your mower(s) via the Automower API. 

Currently, only one mower is supported.

## Installation

1. Backup Your ISY in case of problems!
   * Really, do the backup, please
2. Go to the Polyglot Store in the UI and click Install. You will be redirected to the UDI store to purchase a license for this node server.
3. After purchasing the node server, refresh the store listing.
4. Click the Install button again.
5. After the install completes, go to the dashboard and select Husqvarna 'Details'
6. Configure the node server per configuration section below.


### Node Settings
The settings for this node are:

#### Short Poll
   * Query mower status.

#### Long Poll
   * Not used

#### Username
   * Your Husqvarna account username

#### Password
   * Your Husqvarna account password

## Node substitution variables
 * sys.node.[automow].ST      (Status of mower)
 * sys.node.[automow].GV0     (battery)
 * sys.node.[automow].GV1     (operating mode)
 * sys.node.[automow].GV2     (last error)
 * sys.node.[automow].GV3     (start source)
 * sys.node.[automow].GV4     (start timestamp)
 * sys.node.[automow].GV5     (status mode)
 * sys.node.[automow].GV6     (status activity)
 * sys.node.[automow].GV7     (status state)
 * sys.node.[automow].GV8     (reason)
 * sys.node.[automow].GV9     (status type)


## Requirements
1. A Polisy running Polyglot V3
2. ISY firmware 5.3.x or later
3. An account with Husqvarna


# Release Notes

- 2.0.0 07/18/2021
   - Converted to work with Polyglot version 3
- 1.0.4 08/05/2020
   - fix syntax error
- 1.0.3 08/05/2020
   - re-authenticate if get status fails.
- 1.0.2 10/21/2019
   - handle max retry errors properly.
- 1.0.1 07/23/2019
   - Change mower mode to mowing mode to better reflect what's being reported
   - Fix connection status reporting
- 1.0.0 07/16/2019
   - First public release
- 0.0.2 07/02/2019
   - Updated profile files to add pause command, set the start override period, and added additional status info.
- 0.0.1 05/03/2019
   - Initial version published to github
