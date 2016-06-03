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

   .. py:method:: getDay(int day)
   :returns: $day date
   
   .. py:method:: getSummary(int day)
   :returns: $day weather summary
   
   .. py:method:: getHumidity(int day)
   :returns: $day humidity
   
   .. py:method:: getPrecipProbability(int day)
   :returns: $day precipitations probability
   
   .. py:method:: getMaxTemp(int day)
   :returns: $day max temp
   
   .. py:method:: getMinTemp(int day)
   :returns: $day min temp
   
   .. py:method:: getWindSpeed(int day)
    :returns: $day wind speed
    
    .. py:method:: getSunriseTime(int day)
    :returns: $day sunrise time
    
    .. py:method:: getSunsetTime(int day)
    :returns: $day sunset time
