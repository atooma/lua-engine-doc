=================
LOCATION
=================
This module is needed to get user location.

----------------
Exposed methods
----------------

^^^^^^^^^^^^^^^^^^
getCurrentLocation
^^^^^^^^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
Optionals:

* accuracy ("high" or "low"), defaults to "low"
* locationTimeout (in seconds), defaults to 10s

"""""""""""""
Return value
"""""""""""""
It returns an object with user latitude and longitude.

* getLatitude
* getLongitude

""""""""""""""
Example
""""""""""""""
.. highlight:: lua

::

    loc = location.getCurrentLocation {}
     w = weather.getWeather { latitude = loc:getLatitude(), 
                              longitude = loc:getLongitude(), 
                              numDays = 3 }

