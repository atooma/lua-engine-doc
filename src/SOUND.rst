SOUND
************************

.. module:: sound
   :synopsis: Module needed to set device sound mode

Members
=========================

.. function:: setMode({ mode = "" })

  "Set device sound mode"
    
  :param str mode: mode the device should be put in. One between: "silent", "normal", "vibrate"
  :raises: NO_SUCH_MODE: the specified mode does not exist
  :raises: GENERIC_ERROR: a generic exception occurred
