WEATHER
************************

.. module:: weather
   :synopsis: Module needed to get weather informations

Members
=========================
.. function:: getWeather({ latitude=, longitude=, numDays= })

  "get weather forecasts"
    
  :param double latitude: location's latitude
  :param double longitude: location's longitude
  :param int numDays: number of days for forecasts. Defaults to 1 (today only). OPTIONAL
  :raises: NO_WEATHER_DATA: no data available for required location
  :rtype: :py:class:`weather.WeatherEvent`

.. py:class:: WeatherEvent

   .. py:method:: getSize()
   :returns: number of days forecasts cover

   .. py:method:: getDay()
   :param int day: desired day (from 0 to getSize())
   :returns: $day date
   
   .. py:method:: getSummary()
   :param int day: desired day (from 0 to getSize())
   :returns: $day weather summary
   
   .. py:method:: getHumidity()
   :param int day: desired day (from 0 to getSize())
   :returns: $day humidity
   
   .. py:method:: getPrecipProbability()
   :param int day: desired day (from 0 to getSize())
   :returns: $day precipitations probability
   
   .. py:method:: getMaxTemp()
   :param int day: desired day (from 0 to getSize())
   :returns: $day max temp
   
   .. py:method:: getMinTemp()
   :param int day: desired day (from 0 to getSize())
   :returns: $day min temp
   
   .. py:method:: getWindSpeed()
   :param int day: desired day (from 0 to getSize())
    :returns: $day wind speed
    
    .. py:method:: getSunriseTime()
    :param int day: desired day (from 0 to getSize())
    :returns: $day sunrise time
    
    .. py:method:: getSunsetTime()
    :param int day: desired day (from 0 to getSize())
    :returns: $day sunset time
