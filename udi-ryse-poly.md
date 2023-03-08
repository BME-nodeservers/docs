
# RYSE SmartShades

This node server works with the RYSE SmartShade line of products.  www.helloryse.com

(c) 2023 Robert Paauwe

## Installation

1. Backup Your ISY in case of problems!
   * Really, do the backup, please
2. Go to the Polyglot Store in the UI and install.
3. From the Polyglot dashboard, select the RYSE node server and configure (see configuration options below).
4. Once configured, the RYSE node server should update the IoX with the proper nodes and begin filling in the node data.
5. Restart the Admin Console so that it can properly display the new node server nodes.

### Node Settings
The settings for this node are:

#### Short Poll
   * How often (in seconds) to query the RYSE bridge for updated status.
#### Long Poll
   * Not used
#### Custom Parameters
   * IP address of RYSE bridge

## Node substitution variables

### Smart Shade
 * sys.node.[address].ST    Shade detected and configured
 * sys.node.[address].GV0   Current shade postion (%)
 * sys.node.[address].GV1   Shade position state (moving/stationary)
 * sys.node.[address].GV2   Shade power type (line/battery)
 * sys.node.[address].GV3   Shade power level (%)
 * sys.node.[address].SPEED Shade speed setting

