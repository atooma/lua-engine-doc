TWITTER
************************

.. module:: twitter
   :synopsis: Module that handles interaction with Twitter

Members
=========================
.. function:: requestAuth()

  "Request auth"

  :raises: AUTH_FAIL: auth failed
  :raises: AUTH_NOT_GRANTED: user did not grant auth
  :raises: UNRECOVERABLE_AUTH_EXCEPTION: an unrecoverable exception was thrown
  
  :rtype: :py:class:`AuthOkEvent`
  
  .. py:class:: AuthOkEvent

   .. py:method:: getUserId()
   :returns: userId logged in
   
   .. py:method:: getService()
   :returns: service on which user is logged in
   
   .. py:method:: getScope()
   :returns: scope on which user is logged in
   
.. function:: removeAuth({ userid = "" })

  "Remove auth for userid"
    
  :param str userid: userid
  :raises: ACCOUNT_NOT_FOUND: account could not be found

.. function:: subscribe({ userId = userid, filter = "", subscriberPath = "" })

  "Adds a subscription"
  
  :param str userid: userid
  
.. function:: getTimeline({ userId = userid, limit = })

  "Get user timeline"
  
  :param str userid: userid
  :param int limit: limit to user statuses to be returned
  
  :rtype: :py:class:`TwitterTimelineEvent`
  
  .. py:class:: TwitterTimelineEvent. It is a list of statuses.
