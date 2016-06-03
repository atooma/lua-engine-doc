LOCATION
************************

.. module:: location
   :synopsis: Module that handles interaction with device's location sensor

Members
=========================
.. function:: getCurrentLocation({ accuracy="", locationTimeout="" })

  "get current device location"
    
  :param str accuracy: "high" or "low". Defaults to "low". OPTIONAL
  :param str locationTimeout: timeout of the request, in seconds. Defaults to 10s. OPTIONAL
  :raises: LOCATION_SERVICES_DISABLED: device's location services are disabled
  :raises: GPS_DISABLED: gps is disabled
  :raises: NO_GEOLOCATION_SERVICES: device has no geolocation services
  :raises: LOCATION_TIMEOUT: location request took more than locationTimeout value
  :rtype: :py:class:`location.CurrentLocationEvent`

.. py:class:: CurrentLocationEvent

   .. py:method:: getLatitude()
   :returns: current device's latitude

   .. py:method:: getLongitude()
   :returns: current device's longitude

