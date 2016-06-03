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
   
   .. py:method:: setTime(int hour, int minute, int second, int millisecond)
    :returns: void
    :description: set Hour/Minute/Second/Millisecond of current DateEvent object.
    
   .. py:method:: setDay(int day)
    :returns: void
    :description: add $day to current DateEvent object day.
    
