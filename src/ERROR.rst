=================
ERROR
=================

Every lua method call returns two values:

* an expected object (empty object if nothing needed to be returned)
* an error object, that will be NIL if no error happened.

Even if in all DOC is omitted, every method call that does return something, should be assigned to 2 vars.
Error object will be not NIL if an error occurred.
Error can happen from a variety of different causes, eg: timeout error if the method call is taking too much time, or exception error if an exception was thrown during the method call.
Every module has its own set of error codes, plus an error library with generic errors is always included.

----------------
ERROR CODES
----------------

^^^^^^^^^^^
Generic
^^^^^^^^^^^
* TIMEOUT
* EXCEPTION

^^^^^^^^^^^
Google
^^^^^^^^^^^
* AUTH_FAIL
* AUTH_NOT_GRANTED
* ACCOUNT_NOT_FOUND
* SCOPE_NOT_FOUND
* UNRECOVERABLE_AUTH_EXCEPTION

^^^^^^^^^^^
Gmail
^^^^^^^^^^^
* GMAIL_SEND_FAIL

^^^^^^^^^^^
Gcalendar
^^^^^^^^^^^
* CALENDAR_NOT_FOUND
* CALENDAR_EVENT_NOT_FOUND

^^^^^^^^^^^
Location
^^^^^^^^^^^
* LOCATION_SERVICES_DISABLED
* GPS_DISABLED
* NO_GEOLOCATION_SERVICES
* LOCATION_TIMEOUT

^^^^^^^^^^^
Scheduler
^^^^^^^^^^^
* SCHEDULING_ERROR

^^^^^^^^^^^
Storage
^^^^^^^^^^^
* KEY_NOT_FOUND
* RULE_NOT_FOUND

^^^^^^^^^^^
Weather
^^^^^^^^^^^
* NO_WEATHER_DATA

----------------
Examples
----------------
.. highlight:: lua

::

    auth, err = google.requestAuth { scope = "https://www.googleapis.com/auth/gmail.readonly" }
    if (auth) then
        notification.showNotification { title = "auth", content = "granted" }
    else if (err.code == google.AUTH_NOT_GRANTED) then
        notification.showNotification { title = "auth", content = "not granted" }
    end
    
::

    loc, err = location.getCurrentLocation { locationTimeout = 20 }
    if (loc) then
        n.showNotification { title = "Location", content = tostring(loc:getLatitude()) }
    elseif (err.code == location.LOCATION_SERVICES_DISABLED) then
        n.showNotification { title = "Location", content = "location services disabled." }
    end

