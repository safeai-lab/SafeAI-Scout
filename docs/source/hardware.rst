Hardware
======

System initializations
------

Connect to Power
------
1. **Lidars** 
   All the Lidars and their corresponding power wires are labeled with stickers. The input voltages of the Lidars are 12V. For our current laptop powerbanks, please only connect at mmost 1 Lidar to each power banks, otherwise the output voltage will be unstable, which might lead to unstable sampling frequencey. 

2. **Router** 
   The power wire of the router is labeled and its voltage is also 12V. It can be connected in parallel with any of the lidars.

3. **Xavier** 
   The power wire of Xavier is labeled and its voltage is 20V. It should be connected on a seperate power bank.

Lidar and camera drivers
------
.. code:: bashhh we

   cd pc_ws
