CONTACT
************************

.. module:: contact
   :synopsis: Module needed to get a contact from address book

Members
=========================

.. function:: getContact({ name = "" })

  "Get all contact numbers"
    
  :param str name: user name
  :raises: CONTACT_ERROR: an exception was raised during the process
  :raises: CONTACT_NOT_FOUND: contact could be found

  :rtype: :py:class:`contact.ContactEvent`

  .. py:class:: ContactEvent

   .. py:method:: getSize()
   :returns: number of contacts associated with desired name

   .. py:method:: getContact(int index)
   :returns: returns indexth contact in arraylist of contacts
   :rtype: :py:class:`contact.Contact`
   
   .. py:class:: Contact
   
    .. py:method:: getNumber()
    :returns: contact's number

    .. py:method:: getType()
    :returns: contact's type (ie: "HOME", "MOBILE", "WORK", "UNKNOWN")
