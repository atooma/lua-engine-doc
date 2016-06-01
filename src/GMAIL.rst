GMAIL
************************

.. module:: gmail
   :synopsis: Module that handles interaction with Gmail

Members
=========================
.. function:: sendMail({ sender="", recipient="", subject="", content="" })

  "Send a mail from sender to recipient"

  :param str sender: mail of the sender
  :param str recipient: mail of the recipient
  :param str subject: subject of the mail
  :param str content: content of the mail
  :raises: GMAIL_SEND_FAIL: the mail could not be sent
  :raises: SCOPE_NOT_FOUND
  :raises: ACCOUNT_NOT_FOUND

.. lua:function:: startPubsub({ email = nil })

  "Start the pubsub for the account passed"

  :param str email: mail of the account

.. lua:function:: stopPubsub({ email = nil })

  "Stop the pubsub for the account passed"

  :param str email: mail of the account
