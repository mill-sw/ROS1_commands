### start ros
    roscore 
### check nodes
    rosrun rqt_graph rqt_graph 
### check lists
    rostopic list
### lidar
    cd ydlidar_ws
    catkin_make
    source ./devel/setup.sh
    roslaunch ydlidar_ros_driver X4.launch
### depth-ai camera
    source /opt/ros/melodic/setup.zsh
    rosrun rosserial_python serial_node.py    
