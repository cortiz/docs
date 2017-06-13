.. .. include:: /includes/unicode-checkmark.rst

.. _crafter-profile-api-authentication-persistent_login-create:

=======================
Create Persistent Login
=======================

Creates a persistent login, use for remember me functionality.

--------------------
Resource Information
--------------------

+------------------------------------------------------------------------------------------------+
|| HTTP Verb         | POST                                                                      |
+------------------------------------------------------------------------------------------------+
|| URL               | ``/crafter-profile/api/1/authentication//persistent_login/create``        |
+------------------------------------------------------------------------------------------------+
|| Response Formats  | ``JSON``                                                                  |
+------------------------------------------------------------------------------------------------+

----------
Parameters
----------

+-------------------------+-------------+---------------+-----------------------------------------+
|| Name                   || Type       || Required     || Description                            |
+=========================+=============+===============+=========================================+
|| accessTokenId          || String     || |checkmark|  || The ID of the application access token |
+-------------------------+-------------+---------------+-----------------------------------------+
|| profileId              || String     || |checkmark|  || The ID of the profile                  |
+-------------------------+-------------+---------------+-----------------------------------------+

-------
Example
-------

^^^^^^^
Request
^^^^^^^

.. code-block:: none

  POST .../api/1/authentication/persistent_login/create?accessTokenId=e8f5170c-877b-416f-b70f-4b09772f8e2d&profileId=5925a68def86951f895cf497

^^^^^^^^
Response
^^^^^^^^

``Status 200 OK``

.. code-block:: json

  {
    "tenant": "default",
    "profileId": "5925a68def86951f895cf497",
    "token": "adf88dca-4960-474c-be63-c8c5e3bedaa7",
    "timestamp": 1495665332589,
    "id": "b68c0013-d7b2-4004-8463-d7ba03e15d94"
  }

---------
Responses
---------

+--------+----------------------------------------+----------------------------------------------+
| Status | Location                               | Response Body                                |
+========+========================================+==============================================+
| 200    | ``.../persistent_login/create``        | See example above.                           |
+--------+----------------------------------------+----------------------------------------------+
| 500    |                                        | ``{ "message" : "Internal server error" }``  |
+--------+----------------------------------------+----------------------------------------------+
