FACEBOOK
************************

.. module:: facebook
   :synopsis: Module that handles interaction with Facebook

Members
=========================
.. function:: requestAuth({ scope = "" })

  "Request auth on specified scopes"

  :param str scope: list of scopes
  :raises: AUTH_FAIL: auth failed
  :raises: AUTH_NOT_GRANTED: user did not grant auth
  :raises: SCOPE_NOT_FOUND: scope could not be found
  :raises: UNRECOVERABLE_AUTH_EXCEPTION: an unrecoverable exception was thrown
  
  :rtype: :py:class:`AuthOkEvent`
  
  .. py:class:: AuthOkEvent

   .. py:method:: getUserId()
   :returns: userId logged in
   
   .. py:method:: getService()
   :returns: service on which user is logged in
   
   .. py:method:: getScope()
   :returns: scope on which user is logged in
   
.. function:: removeAuth({ userid = "", scope = "" })

  "Remove auth for userid, on specified scopes"
    
  :param str scope: list of scopes
  :param str userid: userid
  :raises: ACCOUNT_NOT_FOUND: account could not be found
  :raises: SCOPE_NOT_FOUND: scope could not be found

.. function:: addSubscription({ userId = userid, object = "", fields = "" })

  "Adds a subscription on certain user feed"
  
  :param str userid: userid
  :param str object: object type that this subscription applies to
  :param str fields: fields of the subscription
