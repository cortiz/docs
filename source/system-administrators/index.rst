.. _system-administrators:

*********************
System Administrators
*********************

This guide is intended to provide system administrators with the information and access to the tools they need to install and maintain Crafter CMS components.

-------------------
System Requirements
-------------------
+------------------+-----------------------------------+-----------------------------------------+
|| Parameter Name  || Description                      || Prerequisites                          |
+==================+===================================+=========================================+
|| Crafter Studio  || Content authoring server         || Java 1.8+                              |
||                 ||                                  || 1+ Gig of memory to JVM                |
+------------------+-----------------------------------+-----------------------------------------+
|| Crafter Engine  || Content delivery server          || Java 1.8+                              |
||                 ||                                  || 1+ Gig of memory to JVM                |
+------------------+-----------------------------------+-----------------------------------------+
|| Crafter Profile || User profile and attribute store || Java 1.8+                              |
||                 || (Optional component)             || MongoDb 3+                             |
||                 ||                                  || 1+ Gig of memory to JVM                |
+------------------+-----------------------------------+-----------------------------------------+
|| Crafter Social  || User Generated Content server    || Java 1.8+                              |
||                 || (Optional component)             || MongoDb 3+                             |
||                 ||                                  || 1+ Gig of memory to JVM                |
+------------------+-----------------------------------+-----------------------------------------+

* See :ref:`supported platforms<requirements_supported_platforms>` for a detailed list and description of supported components.


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
To Install a Development Environment
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To install a development environment, see :ref:`quick_start_guide`.

----------
Activities
----------

.. toctree::
   :maxdepth: 1
   :titlesonly:

   backup-and-recovery.rst
   rebuilding-studio-database.rst
   debugging-search.rst
   reindexing-content.rst
   upgrading-to-crafter-cms-3-0.rst


---------------
Crafter Studio
---------------

.. toctree::
   :maxdepth: 1
   :titlesonly:

   studio/configure-ldap.rst
   studio/changing-the-studio-logo.rst
   studio/understanding-studio-environment-overrides.rst

--------------
Crafter Engine
--------------

.. toctree::
   :maxdepth: 1
   :titlesonly:

   engine/configure-engine-multi-tenancy.rst
   engine/turning-off-show-error.rst

----------------
Crafter Deployer
----------------

.. toctree::
  :maxdepth: 1
  :titlesonly:

  deployer/admin-guide.rst

--------------
Crafter Search
--------------

.. toctree::
  :maxdepth: 1
  :titlesonly:

  search/index.rst


---------------
Crafter Profile
---------------

.. toctree::
   :maxdepth: 1
   :titlesonly:

   profile/index.rst
   profile/admin/index.rst

--------------
Crafter Social
--------------

.. toctree::
  :maxdepth: 1
  :titlesonly:

  social/index.rst
  social/admin/index.rst



