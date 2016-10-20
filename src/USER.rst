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
   :rtype: :py:class:`Place`

   .. py:method:: getWork()
   :returns: work place
   :rtype: :py:class:`Place`
   
   .. py:class:: Place
    
    .. py:method:: getLatitude()
    :returns: Place's latitude

    .. py:method:: getLongitude()
    :returns: Place's longitude
    
    .. py:method:: getAddress()
    :returns: Place's address
    :rtype: :py:class:`place.Address`
    
     .. py:class:: Address
     
      .. py:method:: getCity()
      :returns: address' city

      .. py:method:: getRoad()
      :returns: address' road
      
      .. py:method:: getPostcode()
      :returns: address' postcode
      
      .. py:method:: getCountryCode()
      :returns: address' country code
      
      .. py:method:: getCountry()
      :returns: address' country
