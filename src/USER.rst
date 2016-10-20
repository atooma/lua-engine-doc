USER
************************

.. module:: user
   :synopsis: Module that handles interaction with user places

Members
=========================

.. function:: getPlaces()

  "Returns user places"

  :rtype: :py:class:`user.UserPlacesEvent`

  .. py:class:: UserPlacesEvent

   .. py:method:: getHome()
   :returns: home place

   .. py:method:: getWork()
   :returns: work place
   :rtype: :py:class:`Place`
   
   .. py:class:: Place
    
    .. py:method:: getLatitude()
    :returns: Place's latitude

    .. py:method:: getLongitude()
    :returns: Place's getLongitude
    
    .. py:method:: getAddress()
    :returns: Place's getAddress
    :rtype: :py:class:`place.Address`
    
     .. py:class:: Address
     
      .. py:method:: getCity()
      :returns: city

      .. py:method:: getRoad()
      :returns: road
      
      .. py:method:: getPostcode()
      :returns: postcode
      
      .. py:method:: getCountryCode()
      :returns: country code
      
      .. py:method:: getCountry()
      :returns: country
