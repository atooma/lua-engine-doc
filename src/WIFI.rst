WIFI
************************

.. module:: wifi
   :synopsis: Module that handles interaction with device's wifi

Members
=========================

.. function:: getWifiStatus()

  "Return current wifi status"

  :rtype: :py:class:`wifi.WifiStatusEvent`

  .. py:class:: WifiStatusEvent

   .. py:method:: getWifiName()
   :returns: current connected wifi name

   .. py:method:: getIp()
   :returns: current ip
   
   .. py:method:: getLinkSpeed()
   :returns: link speed
   
   .. py:method:: getMacAddress()
   :returns: mac address

.. function:: enable()

  "Enables device's wifi"
  
.. function:: disable()
  
  "Disables device's wifi"
