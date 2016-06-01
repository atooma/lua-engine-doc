=================
TIME
=================
This module is needed to get time informations.

----------------
Exposed methods
----------------

^^^^^^^^^^^
getTimezone
^^^^^^^^^^^

"""""""""""""
Return value
"""""""""""""
It returns an object with user timezone ID.

* getId to retrieve ID. (ret: string)

""""""""""""""
Example
""""""""""""""
.. highlight:: lua

::

     tz = time.getTimezone():getId()

^^^^^^^^^^^
getDate
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
Optionals

* timezone ID (defaults to atooma-engine timezone)

"""""""""""""
Return value
"""""""""""""
It returns an object containing current timedate.

* getDate -> returns a rfc3339 string holding current date
* setTime -> change Hour, Minute, Seconds and Milliseconds time
* setDay -> change day

""""""""""""""
Example
""""""""""""""

::
    
    tz = time.getTimezone():getId()
    date = time.getDate { timezone = tz }
    date:setTime(0,0,0,0)
    date:setDay(1)
    notification.showNotification { title = "tomorrow at midnight date", content = date:getDate() }
