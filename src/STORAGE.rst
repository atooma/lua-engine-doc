STORAGE
************************

.. module:: storage
   :synopsis: Module needed to store strings/objects from within a rule
   
Members
=========================
.. function:: put({ key = "", value =  })

  "Store value object with key"
  
  :param str key: value's associated key
  :param str value: string or object to be stored
  
.. function:: get{ key = "" })

  "Get stored key value"

  :param str key: desired stored object key
