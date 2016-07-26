ALARM
************************

.. module:: alarm
   :synopsis: Module needed to manage phone's alarm clock

Members
=========================

.. function:: setAlarm({ hours = , minutes =  })

  "Set an alarm"
    
  :param int hours: desired alarm hours
  :param int minutes: desired alarm minutes
  :raises: ALARM_ERROR: a generic exception occurred
  
.. function:: getAlarm()
  
  "Get nearest alarm"
  
  :raises: NO_ALARM: there are no alarms setAlarm
  :rtype: :py:class:`alarm.AlarmClockEvent`
  
  .. py:class:: AlarmClockEvent

   .. py:method:: getTime()
   :returns: time String of nearest alarm

