### start ros
    roscore 
### check nodes
    rosrun rqt_graph rqt_graph 
### check lists
    rostopic list
### listen raw data
    rostopic echo {/topic name}
### visualize data
    rviz
    rosrun rqt_image_view rqt_image_view
### lidar
    source ydlidar_ws/devel/setup.zsh
    cd ydlidar_ws
    catkin_make
    source ./devel/setup.zsh
    #source ./devel/setup.sh
    roslaunch ydlidar_ros_driver X4.launch
### depth-ai camera
    source depthai_ws/devel/setup.zsh
    roslaunch depthai_examples stereo_node.launch
### arduino
    sudo chmod 666 /dev/ttyACM0
    rosrun rosserial_python serial_node.py _port:=/dev/ttyACM0 _baud:=57600
    
