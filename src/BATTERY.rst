BATTERY
************************

.. module:: battery
   :synopsis: Module that handles interaction with the device battery

Members
=========================

.. function:: getBatteryStatus()

  "Return the current Battery status"

  :rtype: :py:class:`battery.BatteryStatusEvent

.. py:class:: BatteryStatusEvent

   .. py:method:: isCharging()
   :returns: true if the battery is charging

   .. py:method:: isUsbCharge()
   
   .. py:method:: isAcCharge()
   
   .. py:method:: getLevel()


    
