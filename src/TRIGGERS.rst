TRIGGERS
************************

There are some functions that can be called from any lua rules, and that are binded to certain events.
When one of these events gets triggered, the corresponding function gets called with the indicated parameter.

Members
=========================

.. function:: onGmailMailEvent(GmailMailEvent)

  "Called when a new mail is received from a gmail pubsub. Obviously proper auth and gmail.startPubSub() call are needed."
    
  :param GmailMailEvent event: event that holds info about new mail
  
.. function:: onBatteryLowLevelEvent()
  
  "Called when device battery goes below a threshold (android defined)."
  
.. function:: onBatteryPowerDisconnectedEvent()

  "Called when ac gets disconnected from device."
  
.. function:: onBatteryPowerConnectedEvent()

  "Called when ac gets connected to device."

.. function:: onGcalendarEvent(GcalendarEvent)

  "Called when a new gcalendar event is received from a gcalendar pubsub. Obviously proper auth and gcalendar.startPubSub() call are needed."
    
  :param GcalendarEvent event: event that holds info about new calendar event
  
.. function:: onGcalendarTimeoutEvent(GcalendarEvent)

  "Called when the alarm created on a gcalendarEvent with gcalendar.scheduleAlarm() expires."
    
  :param GcalendarEvent event: event that holds info about the calendar event
  
.. function:: onFacebookPostEvent(FacebookPostEvent)

  "Called when a new post is received from facebook subscription. Obviously it needs proper facebook auth and subscription."
  
  :param FacebookPostEvent event: event that holds info about new facebook post
  
.. function:: onLocationGeofenceTriggerEvent(LocationGeofenceTriggerEvent)

  "Called when a geofence gets triggered. Geofence has to be created with location.addGeofence() method."
  
  :param LocationGeofenceTriggerEvent event: event that holds info about geofence trigger.
  
.. function:: onUserAtHomeEvent()

  "Called when user is detected entering home. Our sdk provides this function without any need to manually add any geofence."
  
.. function:: onUserAtWorkEvent()

  "Called when user is detected entering work place. Our sdk provides this function without any need to manually add any geofence."
  
.. function:: onUserLeftHomeEvent()

  "Called when user is detected leaving home. Our sdk provides this function without any need to manually add any geofence."
  
.. function:: onUserLeftWorkEvent()

  "Called when user is detected leaving work place. Our sdk provides this function without any need to manually add any geofence."
  
.. function:: onHeadsetPlugEvent()

  "Called when device detects headset plugging."
  
.. function:: onWifiEnabledEvent()

  "Called when device's wifi get enabled."
