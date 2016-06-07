BATTERY
************************

.. module:: battery
   :synopsis: Module that handles interaction with the device battery

Members
=========================

.. function:: getBatteryStatus()

  "Return the current Battery status"

  :rtype: :py:class:`battery.BatteryStatusEvent`

  .. py:class:: BatteryStatusEvent

   .. py:method:: isCharging()
   :returns: true if the battery is charging

   .. py:method:: isUsbCharge()
   :returns: true if the battery is charging through usb
   
   .. py:method:: isAcCharge()
   :returns: true if the battery is charging through AC
   
   .. py:method:: getLevel()
   :returns: battery level

