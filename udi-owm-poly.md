
# OpenWeatherMaps weather service plug-in

This plug-in uses the OpenWeatherMap weather service to obtain current
weather conditions and forecast weather conditions data.

This data may be used in IoX programs as trigger conditions.

To access dta from the OpenWeatherMap weather service you will need an 
account with openweathermap.org and a subscription to their weather service.

The plug-in works only with the "One Call 3.0" subscription plan and not any of the plans that are part of the "Professional Collections".  More information
on the subscription plans and costs are available at
[OpenWeatherMap](http://openweathermap.org/api)

The "One Call 3.0" subscription plan allows for a limited number of "Free" 
API calls per day. The current limit is 1000 which means that the short poll
interval must be configured to at least 87 seconds.  The default value is 600 
seconds.

To get data more offen that once every 87 seconds, you will need to pay OpenWeatherMap for additional calls.

## Node substituion variables
### Current condition node
 * sys.node.[address].ST      (Node sever online)
 * sys.node.[address].CLITEMP (current temperature)
 * sys.node.[address].CLIHUM  (current humidity)
 * sys.node.[address].BARPRES (current barometric pressure)
 * sys.node.[address].WINDDIR (current wind direction )
 * sys.node.[address].DISTANC (current visibility)
 * sys.node.[address].DEWPT   (current dew point temperature)
 * sys.node.[address].UV      (current UV index)
 * sys.node.[address].GV2     (current feels like temperature)
 * sys.node.[address].GV4     (current wind speed)
 * sys.node.[address].GV6     (current rain rate)
 * sys.node.[address].GV7     (current snow rate)
 * sys.node.[address].GV13    (current conditions)
 * sys.node.[address].GV14    (current percent cloud coverage)
 * sys.node.[address].GV18    (current percent chance of precipitation)

 ### Forecast node
 * sys.node.[address].CLIHUM  (forecasted humidity)
 * sys.node.[address].BARPRES (forecasted barometric pressure)
 * sys.node.[address].DEWPT   (forecasted dew point temperature)
 * sys.node.[address].UV      (forecasted max UV index)
 * sys.node.[address].GV19    (day of week forecast is for)
 * sys.node.[address].GV0     (forecasted high temperature)
 * sys.node.[address].GV1     (forecasted low temperature)
 * sys.node.[address].GV2     (forecasted daytime feels like temperature)
 * sys.node.[address].GV13    (forecasted conditions)
 * sys.node.[address].GV14    (forecasted percent cloud coverage)
 * sys.node.[address].GV4     (forecasted wind speed)
 * sys.node.[address].GV6     (forecasted rain)
 * sys.node.[address].GV7     (forecasted snow)
 * sys.node.[address].GV18    (forecasted percent chance of precipitation)
 * sys.node.[address].GV20    (calculated ETo for the day)
 * sys.node.[address].GV21    (forecasted icon URL)

