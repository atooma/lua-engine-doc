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

* isCharging (ret: boolean)
* isUsbCharge (ret: boolean)
* isAcCharge (ret: boolean)
* getLevel (ret: float)

""""""""""""""
Example
""""""""""""""
.. highlight:: lua

::

    battery.getBatteryStatus {}
    notification.showNotification { title = "battery level", content = tostring(batt:getLevel()) }
    
