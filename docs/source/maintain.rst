maintain
======

Adjust fan mode
------

Set fan to cooling mode if Xavier is too hot

.. code:: bash

   sudo /usr/sbin/nvpmodel -d "cool"

Set fan to quite mode if Xavier is normal

.. code:: bash

   sudo /usr/sbin/nvpmodel -d "quiet"

