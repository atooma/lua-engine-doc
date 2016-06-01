=================
GCALENDAR
=================
This module is needed to manage user calendars.

----------------
Exposed methods
----------------

^^^^^^^^^^^
startPubSub
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* email (string)

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""
.. highlight:: lua

::

    gcalendar.startPubSub { email = "xxxxxx@gmail.com" }
    
^^^^^^^^^^^
stopPubSub
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* email (string)

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""

::

    gcalendar.stopPubSub { email = "xxxxxx@gmail.com" }

^^^^^^^^^^^
getEvents
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* calendar object

Optionals:

* timeMax (string)
* timeMin (string)

If not specified, getEvents will retrieve every calendar's event.

"""""""""""""
Return value
"""""""""""""
It returns an object that lists every event in the specified time frame.

* getSize (ret: int -> number of events)
* getEvents (ret: arraylist)
* getEvent(int index) (ret: calendar event object)

""""""""""""""
Example
""""""""""""""

::

    calEvents = gcalendar.getEvents { calendar = calendar, timeMax = to, timeMin = from }
    for i = 0, calEvents:getSize()-1 do
        evt = calEvents:getEvent(i)
        print evt:getSummary()
    end
    
^^^^^^^^^^^
addEvent
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* calendar object
* startTime
* endTime

Optionals:

* description
* location
* summary

"""""""""""""
Return value
"""""""""""""
It returns a gcalendar event object with event's specified field. Retrieve them with:

* getCreator (ret: string)
* getSummary (ret : string)
* getId (ret: string)
* getLocation (ret: string)
* getDescription (ret: string)
* getStart (ret: string)
* getEnd (ret: string)

""""""""""""""
Example
""""""""""""""

::

        event = gcalendar.addEvent { calendar = calendar,
                                     startTime = "2016-05-25T17:59:30",
                                     endTime = "2016-05-26T12:18:30", 
                                     description = "Atooma test", 
                                     location = "Rome", 
                                     summary = "top" }
                                 
^^^^^^^^^^^
getCalendar
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* email

Optionals:

* calendarId, defaults to "primary"

"""""""""""""
Return value
"""""""""""""
It returns a calendar object needed to call other gcalendarLib methods.

""""""""""""""
Example
""""""""""""""

::

    gcalendar.getCalendar { email = "xxxxx@gmail.com" }

^^^^^^^^^^^
removeEvent
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* gcalendar event ID
* calendar object

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""

::

    gcalendar.removeEvent { calendar = calendar, id = "xxxxxxxxxxx" }

^^^^^^^^^^^^^
scheduleAlarm
^^^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* gcalendar event ID
* calendar object
* before OR after integer values

Optionals:

* interval
* times

* before: seconds before event start time when user wants to be notified.
* after: seconds after event end time when user wants to be notified.
* interval: interval in seconds for each notification, when times is set
* times: number of times we want a notification to be sent, with $interval sec between them.

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""

::

    gcalendar.scheduleAlarm { calendar = calendar, id = "xxxxxx", after = 60, interval = 10, times = 5 }

^^^^^^^^^^^
removeAlarm
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* gcalendar event ID
* alarmType

* alarmType: "After" or "Before". Type of alarm you want to delete.

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""

::

    gcalendar.removeAlarm { id = "xxxxxxxx", alarmType = "After" }
