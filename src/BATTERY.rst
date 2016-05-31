=================
BATTERY
=================
This module is needed to manage battery.

----------------
Exposed methods
----------------

^^^^^^^^^^^^^^^^
getBatteryStatus
^^^^^^^^^^^^^^^^

"""""""""""""
Return value
"""""""""""""
It returns an object holding current battery info.
Retrieve them with these methods:

* getCharging (boolean)
* getUsbCharge (boolean)
* getAcCharge (boolean)
* getLevel (float)

""""""""""""""
Example
""""""""""""""
.. highlight:: lua

::

    battery.getBatteryStatus {}
    notification.showNotification { title = "battery level", content = tostring(batt:getLevel()) }
    
