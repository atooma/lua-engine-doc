=================
GOOGLE
=================
This module is needed to manage auth requests for current user.

----------------
Exposed methods
----------------

^^^^^^^^^^^
requestAuth
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* scope

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""
.. highlight:: lua

::

    google.requestAuth { scope = "https://www.googleapis.com/auth/calendar.readonly https://www.googleapis.com/auth/gmail.compose" }

^^^^^^^^^^^
removeAuth
^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* scope
* email

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""

::

    google.removeAuth { scope = "https://www.googleapis.com/auth/calendar.readonly https://www.googleapis.com/auth/gmail.compose", email = "xxxxxxx@gmail.com" }

