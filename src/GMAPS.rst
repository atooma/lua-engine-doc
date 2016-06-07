GMAPS
************************

.. module:: gmaps
   :synopsis: Module that handles interaction with Gmaps

Members
=========================
.. function:: geocode({ address = "" })

  "Get latitude and longitude from given address"

  :param str address: location's address
  :rtype: :py:class:`gmaps.GmapsGeocodeEvent`
  
  .. py:class:: GmapsGeocodeEvent

   .. py:method:: getPlaceId()
   :returns: gmaps place Id

   .. py:method:: getAddress()
   :returns: address
   
   .. py:method:: getLatitude()
   :returns: place's latitude
   
    .. py:method:: getLongitude()
   :returns: place's longitude

.. function:: reverseGeocode({ latitude = , longitude =  })

  "Return address of given coordinates"

  :param double latitude: latitude of desired place
  :param double longitude: longitude of desired place
  :rtype: :py:class:`gmaps.GmapsGeocodeEvent`

.. function:: getDistance({ lat=, lon=, destLat=, destLon=, travelMode="", avoid="", arrivalTime=, departureTime=, transitMode="" })

  "Return distance and travel time between two places"
  
  Check gmaps doc for arguments values: https://developers.google.com/maps/documentation/distance-matrix/intro#DistanceMatrixRequests

  :param double lat: latitude of starting place
  :param double lon: longitude of starting place
  :param double destLat: latitude of destination place
  :param double destLon: longitude of destination place
  :param str travelMode: travel mode. Defaults to DRIVING. OPTIONAL
  :param str avoid: avoid certain roads (eg highways). No default value. OPTIONAL
  :param int arrivalTime: desired arrival time in epoch. No default value. OPTIONAL
  :param int departureTime: departure time in epoch. No default value. OPTIONAL
  :param str transitMode: if travelMode == TRANSIT, specifies mean of transport. No default value. OPTIONAL
  :rtype: :py:class:`gmaps.GmapsDistanceMatrixEvent`
  
.. py:class:: GmapsDistanceMatrixEvent

   .. py:method:: getDistance()
   :returns: distance in meters

   .. py:method:: getDuration()
   :returns: travel duration in seconds
   
   .. py:method:: getDurationHumanReadable()
   :returns: travel duration human readable
   
   .. py:method:: getDurationInTraffic()
   :returns: travel duration based on current and historical traffic
   
   .. py:method:: getDurationInTrafficHumanReadable()
   :returns: travel duration based on current and historical traffic human readable
   
.. function:: searchNearBy({ latitude=, longitude=, radius=, name="", minPrice="", maxPrice="", openNow=, rankBy="", type"" })

  "Get nearby places"
  
  Check gmaps doc for arguments values: https://developers.google.com/places/web-service/search#PlaceSearchRequests
  
  :param double latitude: latitude of desired place
  :param double longitude: longitude of desired place
  :param double radius: radius to search for places
  :param str name: name to search for in nearBy places. No def value. OPTIONAL
  :param str minPrice: minimum price for places to be included in results. Defaults to UNKNOWN. OPTIONAL
  :param str maxPrice: maximum price for places to be included in results. Defaults to UNKNOWN. OPTIONAL
  :param bool openNow: whether to only include open places in results. Defaults to false. OPTIONAL
  :param str rankBy: sorting function for places. Defaults to prominence. OPTIONAL
  :param str type: type of places to look for. No def value. OPTIONAL
  :rtype: :py:class:`gmaps.GmapsSearchEvent`
  
  .. py:class:: GmapsSearchEvent

   .. py:method:: getSize()
   :returns: number of found places

   .. py:method:: getPlaces()
   :returns: arraylist of places
   
   .. py:method:: getPlace(int index)
   :returns: returns indexth place in arraylist of places
   :rtype: :py:class:`gmaps.GmapsPlace`
   
   .. py:class:: GmapsPlace
   
    .. py:method:: getName()
    :returns: place's name

    .. py:method:: getAddress()
    :returns: place's address
   
    .. py:method:: getLatitude()
    :returns: place's latitude
    
    .. py:method:: getLongitude()
    :returns: place's longitude
    
    .. py:method:: getPlaceId()
    :returns: gmaps placeId
    
    .. py:method:: getVicinity()
    :returns: feature name of a nearby location
    
    .. py:method:: getRating()
    :returns: gmaps place's rating
   
   
.. function:: placeDetails({ placeId="" })

  "Retrieve place's info"
  
  :param str placeId: gmaps desired place's id
  :rtype: :py:class:`gmaps.GmapsDetailsEvent`
  
  .. py:class:: GmapsDetailsEvent

   .. py:method:: getAddress()
   :returns: place's address

   .. py:method:: getPhoneNumber()
   :returns: place's phone number
   
   .. py:method:: getLatitude()
   :returns: place's latitude
   
   .. py:method:: getLongitude()
   :returns: place's longitude

   .. py:method:: getName()
   :returns: place's name
   
   .. py:method:: getPriceLevel()
   :returns: place's price level
   
   .. py:method:: getRating()
   :returns: place's rating

   .. py:method:: getVicinity()
   :returns: feature name of a nearby location
   
   .. py:method:: getWebsite()
   :returns: place's website
