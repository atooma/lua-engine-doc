===================
NOTIFICATION
===================
This module is needed to push notifications to user phone.

----------------
Exposed methods
----------------

^^^^^^^^^^^^^^^^^^
showNotification
^^^^^^^^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* title
* content

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""
.. highlight:: lua

::

    notification.showNotification { title = "hello", content = "world" }

^^^^^^^^^^^^^^^^^^
showToast
^^^^^^^^^^^^^^^^^^

"""""""""""
Arguments
"""""""""""
**Required**:

* content

"""""""""""""
Return value
"""""""""""""
It returns an empty object if everything was successful, or NIL if an error happened.

""""""""""""""
Example
""""""""""""""
.. highlight:: lua

::

    notification.showTOast { content = "hello world" }
