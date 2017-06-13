.. .. include:: /includes/unicode-checkmark.rst

.. _crafter-engine-api-site-mappings-reload:

===============
Reload Mappings
===============

Reload the mapping used to resolve sites by Crafter Engine.
This endpoint is opnly available when Crafter Engine is configured as multi-tenant.

--------------------
Resource Information
--------------------

+----------------------------+-------------------------------------------------------------------+
|| HTTP Verb                 || GET                                                              |
+----------------------------+-------------------------------------------------------------------+
|| URL                       || ``/api/1/site/mappings/reload``                                  |
+----------------------------+-------------------------------------------------------------------+
|| Response Formats          || ``JSON``                                                         |
+----------------------------+-------------------------------------------------------------------+

-------
Example
-------

^^^^^^^
Request
^^^^^^^

``GET .../api/1/site/mappings/reload``

^^^^^^^^
Response
^^^^^^^^

``Status 200 OK``

.. code-block:: json

  { "message": "Mappings reloaded" }

---------
Responses
---------

+--------+------------------------------+--------------------------------------------------------+
|| Status|| Location                    || Response Body                                         |
+========+==============================+========================================================+
|| 200   || ``.../site/mappings/reload``|| See example above.                                    |
+--------+------------------------------+--------------------------------------------------------+
|| 200   ||                             | .. code-block:: json                                   |
||       ||                             |                                                        |
||       ||                             |   { "message" : "The current resolver is not a         |
||       ||                             |   ReloadableMappingsSiteResolver. No mappings to       |
||       ||                             |   reload" }                                            |
+--------+------------------------------+--------------------------------------------------------+
