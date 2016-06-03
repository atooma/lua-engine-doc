GOOGLE
************************

.. module:: google
   :synopsis: Module that handles interaction with Google

Members
=========================
.. function:: requestAuth({ scope = "" })

  "Request auth on specified scopes"

  :param str scope: list of scopes
  :raises: AUTH_FAIL: auth failed
  :raises: AUTH_NOT_GRANTED: user did not grant auth
  :raises: SCOPE_NOT_FOUND: scope could not be found
  :raises: UNRECOVERABLE_AUTH_EXCEPTION: an unrecoverable exception was thrown
    
.. function:: removeAuth({ email = "", scope = "" })

  "Remove auth for email user, on specified scopes"
    
  :param str scope: list of scopes
  :param str email: user mail address
  :raises: ACCOUNT_NOT_FOUND: account could not be found
  :raises: SCOPE_NOT_FOUND: scope could not be found

