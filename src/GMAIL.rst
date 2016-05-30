=================
GMAIL
=================
This module is needed to manage gmail.

----------------
Exposed methods
----------------

^^^^^^^^^^^
sendMail
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* Sender
* Recipient
* Subject
* Content

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""
.. highlight:: lua

::

    gmail.sendMail { sender = email, 
                     recipient = email, 
                     subject = "test",
                     content = text }

^^^^^^^^^^^
startPubSub
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* email

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""

::

    gmail.startPubSub { email = "xxxxxx@gmail.com" }

^^^^^^^^^^^
stopPubSub
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* email

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""

::

    gmail.stopPubSub { email = "xxxxxx@gmail.com" }
