NOTIFICATION
************************

.. module:: notification
   :synopsis: Module that handles notification sending to android device

Members
=========================
.. function:: showNotification({ title = "", content = "" })

  "Send a notification to android device"
  
  :param str title: notification's title
  :param str content: notification's content
  
.. function:: showToast({ content = "" })

  "Send a toast notification to android device"

  :param str content: notification's content
