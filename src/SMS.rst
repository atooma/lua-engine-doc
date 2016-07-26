SMS
************************

.. module:: sms
   :synopsis: Module needed to send sms

Members
=========================

.. function:: sendSMS({ phoneNumber = "", text = "" })

  "Send a sms"
    
  :param str phoneNumber: user phone number
  :param str text: text to be sent
  :raises: SMS_NOT_SENT: could not send sms

