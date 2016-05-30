=================
WEATHER
=================
This module is needed to get weather data from forecastIO.

----------------
Exposed methods
----------------

^^^^^^^^^^^
getWeather
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* latitude, longitude

Optionals:

* numDays -> Number of days forecasts should cover. Defaults to 1 (today only) if not explicitly set.

"""""""""""""
Return value
"""""""""""""
It returns an object with lots of information. Retrieve them with these methods:

* getDay
* getSummary
* getHumidity
* getPrecipProbability
* getMaxTemp
* getMinTemp
* getWindSpeed
* getSunriseTime
* getSunsetTime

""""""""""""""
Example
""""""""""""""
.. highlight:: lua

::

    w = weather.getWeather { latitude = loc:getLatitude(), 
                             longitude = loc:getLongitude(), 
                             numDays = 3 }

