Perception
======

Camera-lidar Calibration
------

This part uses Livox’s official calibration `package <https://github.com/Livox-SDK/livox_camera_lidar_calibration/blob/master/doc_resources/README_cn.md>`_
.. note::

   The camera has already been calibrated:
   
   .. image:: calib.png
   :width: 600

Sampling
~~~~~~

 #. Camera sampling
 
    * `Script <https://github.com/jiarunw/jiarun_zed/blob/main/image_capture.py>`_
    
 #. Lidar sampling
 
    #. Launch the front lidar: 
    
       .. code:: 
          
          roslaunch livox_ros_driver livox_lidar_msg.launch
    
    #. Record a ros bag for 10 seconds: 
    
       .. code::
       
          rosbag record /livox/lidar_3GGDJ1500107361

   

