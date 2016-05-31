=================
WIFI
=================
This module is needed to manage wifi.

----------------
Exposed methods
----------------

^^^^^^^^^^^^^^
getWifiStatus
^^^^^^^^^^^^^^

"""""""""""""
Return value
"""""""""""""
It returns an object holding current wifi info.
Retrieve them with these methods:

* getWifiName (string)
* getIp (int)
* getLinkSpeed (int)
* getMacAddress (string)

""""""""""""""
Example
""""""""""""""
.. highlight:: lua

::

    name = wifi.getWifiStatus {}
    notification.showNotificaton { title = "wifi", content = name:getWifiName() }


^^^^^^^^^
enable
^^^^^^^^^

"""""""""""""
Return value
"""""""""""""
It does return anything.

""""""""""""""
Example
""""""""""""""

::

    wifi.enable {}

    
^^^^^^^^^
disable
^^^^^^^^^

"""""""""""""
Return value
"""""""""""""
It does return anything.

""""""""""""""
Example
""""""""""""""

::

    wifi.disable {}
