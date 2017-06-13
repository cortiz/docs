.. .. include:: /includes/unicode-checkmark.rst

.. _crafter-profile-api-profile-range:

=====================
Get Profiles By Range
=====================

Returns a range of profiles for the specified tenant.

--------------------
Resource Information
--------------------

+----------------------------+-------------------------------------------------------------------+
|| HTTP Verb                 || GET                                                              |
+----------------------------+-------------------------------------------------------------------+
|| URL                       || ``/crafter-profile/api/1/profile/range``                         |
+----------------------------+-------------------------------------------------------------------+
|| Response Formats          || ``JSON``                                                         |
+----------------------------+-------------------------------------------------------------------+

----------
Parameters
----------

+-------------------+-------------+---------------+----------------------------------------------+
|| Name             || Type       || Required     || Description                                 |
+===================+=============+===============+==============================================+
|| accessTokenId    || String     || |checkmark|  || The ID of the application access token      |
+-------------------+-------------+---------------+----------------------------------------------+
|| tenantName       || String     || |checkmark|  || The tenant's name                           |
+-------------------+-------------+---------------+----------------------------------------------+
|| sortBy           || String     ||              || Profile attribute to sort the list by       |
+-------------------+-------------+---------------+----------------------------------------------+
|| sortOrder        || String     ||              || The sort order (either ASC or DESC)         |
+-------------------+-------------+---------------+----------------------------------------------+
|| start            || String     ||              || From the entire list of results, the        |
||                  ||            ||              || position where the actual results should    |
||                  ||            ||              || start (useful for pagination)               |
+-------------------+-------------+---------------+----------------------------------------------+
|| count            || String     ||              || The number of profiles to return            |
+-------------------+-------------+---------------+----------------------------------------------+
|| attributeToReturn|| String     ||              || The name of the attributes to return        |
||                  ||            ||              || (don't specify to return all)               |
+-------------------+-------------+---------------+----------------------------------------------+

-------
Example
-------

^^^^^^^
Request
^^^^^^^

.. code-block:: none

  GET .../api/1/profile/range?accessTokenId=e8f5170c-877b-416f-b70f-4b09772f8e2d&tenantName=sample-tenant

^^^^^^^^
Response
^^^^^^^^

``Status 200 OK``

.. code-block:: json

  [
    {
      "username": "john.doe",
      "email": "john.doe@example.com",
      "verified": false,
      "enabled": false,
      "createdOn": 1495811673842,
      "lastModified": 1495811673842,
      "tenant": "sample-tenant",
      "roles": [],
      "attributes": {},
      "id": "59284659d4c650213cc2f3fc"
    }
  ]

---------
Responses
---------

+---------+--------------------------------+-----------------------------------------------------+
|| Status || Location                      || Response Body                                      |
+=========+================================+=====================================================+
|| 200    || ``.../profile/range``         || See example above.                                 |
+---------+--------------------------------+-----------------------------------------------------+
|| 500    ||                               || ``{ "message" : "Internal server error" }``        |
+---------+--------------------------------+-----------------------------------------------------+
