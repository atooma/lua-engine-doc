TIME
************************

.. module:: time
   :synopsis: Module that exposes time related methods

Members
=========================
.. function:: getTimezone()

  "Get device's timezone"
  
  :rtype: :py:class:`time.TimezoneEvent`

.. py:class:: TimezoneEvent

   .. py:method:: getId()
   :returns: timezone ID

.. function:: getDate()

  "Get current timedate"
  
  :param str timezone: timezone ID
  
  :rtype: :py:class:`time.DateEvent`

.. py:class:: DateEvent

   .. py:method:: getDate()
   :returns: rfc3339 string of current date
   
   .. py:method:: setTime()
    :returns: void
    :description: set Hour/Minute/Second/Millisecond of current DateEvent object.
    :param int hour: set current DateEvent hour
    :param int minute: set current DateEvent minute
    :param int second: set current DateEvent second
    :param int millisecond: set current DateEvent millisecond
    
   .. py:method:: setDay()
    :returns: void
    :description: set Day of current DateEvent object.
    :param int day: move Date $day forward/backward (if $day < 0)
    
