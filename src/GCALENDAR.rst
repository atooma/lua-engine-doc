GCALENDAR
************************

.. module:: gcalendar
   :synopsis: Module that handles interaction with GCalendar

Members
=========================
.. function:: startPubsub({ email = "" })

  "Start the pubsub for the account passed"

  :param str email: mail of the account

.. function:: stopPubsub({ email = "" })

  "Stop the pubsub for the account passed"

  :param str email: mail of the account

.. function:: getEvents({ calendar=nil, timeMax="", timeMin="" })

  "Retrieve all the events in the calendar of the user"

  :param instance calendar: :py:class:`gcalendar.GCalendarCalendar`
  :param str timeMix: from which date retrieve events. Defaults to first calendar's event. OPTIONAL
  :param str timeMax: till which date retrieve events. Defaults to now. OPTIONAL
  :raises: SCOPE_NOT_FOUND
  :raises: ACCOUNT_NOT_FOUND
  :raises: CALENDAR_NOT_FOUND
  :rtype: :py:class:`gcalendar.GcalendarEventsEvent`
  
  
.. py:class:: GcalendarEventsEvent

   .. py:method:: getSize()
   :returns: number of events

   .. py:method:: getEvents()
   :returns: arraylist of all events found
   
   .. py:method:: getEvent(int index)
   :returns: GcalendarEvent object
   
.. function:: addEvent({ calendar=nil, startTime="", endTime="", description = "", location = "", summary = "" })

  "Add a calendar event"
  
  :param instance calendar: :py:class:`gcalendar.GCalendarCalendar`
  :param str startTime: starting time of the event
  :param str endTime: ending time of the event
  :param description: event description. OPTIONAL
  :param str location: event location. OPTIONAL
  :param str summary: event summary. OPTIONAL
  :rtype: :py:class:`gcalendar.GcalendarEvent`
  
  .. py:class:: GcalendarEvent

   .. py:method:: getCreator()
   :returns: event creator

   .. py:method:: getSummary()
   :returns: event summary
   
   .. py:method:: getId()
   :returns: event gcalendar id
   
   .. py:method:: getLocation()
   :returns: event location

   .. py:method:: getDescription()
   :returns: event description
   
   .. py:method:: getStart()
   :returns: event start time

   .. py:method:: getEnd()
   :returns: event end time

.. function:: getCalendar({ email="", calendarId = "" })

  "Retrieve a GCalendarCalendar object"
  
  :param str email: user email
  :param str calendarId: user desired calendarId. Defaults to "primary". OPTIONAL
  :rtype: :py:class:`gcalendar.GCalendarCalendar`
  
  .. py:class:: GCalendarCalendar

   .. py:method:: getEmail()
   :returns: calendar object email

   .. py:method:: getTimezone()
   :returns: calendar timezone
   
   .. py:method:: getId()
   :returns: calendar id

   
.. function:: removeEvent({ calendar=nil, id="" })

  "Remove a calendar event"

  :param instance calendar: :py:class:`gcalendar.GCalendarCalendar`
  :param str id: gcalendar event id

.. function:: scheduleAlarm({ calendar=nil, id="", before= , after=, interval=, times= })

  "Schedule an alarm on calendar event"

  :param instance calendar: :py:class:`gcalendar.GCalendarCalendar`
  :param str id: gcalendar event id
  :param int before: seconds to schedule alarm before event start
  :param int after: seconds to schedule alarm after event end
  :param int interval: interval in seconds between each notification, when times is set. Defaults to off. OPTIONAL
  :param int after: number of times we want a notification to be sent, with $interval sec between them. Defaults to 1. OPTIONAL
  
.. function:: removeAlarm({ id="", alarmType="" })

  "Schedule an alarm on calendar event"

  :param str alarmType: Whether to remove an "after" or "before" alarm for the event
  :param str id: gcalendar event id
