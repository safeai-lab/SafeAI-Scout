Hardware
======

System initializations
------

* Power Connection
   1. **Lidars** 
      All the Lidars and their corresponding power wires are labeled with stickers. The input voltages of the Lidars are 12V. For our current laptop powerbanks, please only connect at mmost 1 Lidar to each power banks, otherwise the output voltage will be unstable, which might lead to unstable sampling frequencey. 

   2. **Router** 
      The power wire of the router is labeled and its voltage is also 12V. It can be connected in parallel with any of the lidars.

   3. **Xavier** 
      The power wire of Xavier is labeled and its voltage is 20V. It should be connected on a seperate power bank.

* Data Transfer Connection 
   1. **Lidars**
      Each lidar is connected to the router with a ethernet cable respectively
   2. **Xavier**
      The processor is connected to the Lidars via the router through ethernet cable.
   3. **Camera**
      The ZED2 camera is connected to the processor via USB.
   4. **Chassis**
      The chassis is connected to the processor via USB in CAN protocol.

* Remote Controller Connection
   As is shown in the following figure, the buttons and joysticks are labeled with numbers. To turn the controller on and connect the chassis, follow these steps: 
   
   1. Flip `lever 1`, `lever 2`, `lever 3` and `lever 4` to the top
  
   2. Hold `button 5` and `button 6`
  
   3. Flip `lever 1` to the bottom and `lever 2` to the middle.
   
   4. Turn on the chassis and wait for connection in approximately 5 seconds.
   
   Detailed Manual can be found  `here <https://www.generationrobots.com/media/agilex/SCOUT_MINI_UserManual_v1.0.1_EN.pdf>`_, the configuration of the controller can be found `here <松灵机器人产品遥控器校准配置指导手册_v1.0_CN.pdf>`_
   
   .. image:: controller.jpg
      :width: 400px
      


Lidar and camera drivers
------
.. code:: bash

   cd pc_ws
   sudo ifconfig eth0 192.168.1.50
   sudo ptp4l -l eth0 -l -6 -m
   sudo phc2sys -c eth0 -s CLOCK_REALTIME -o 0
