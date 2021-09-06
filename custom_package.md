### custom package
    mkdir -p <ws_name>/src/<package_dir_name>
    cd <ws_name>/src
    catkin_create_pkg <package_dir_name> <package_type:ie.std_msgs> <package_language:ie:roscpp>
    
    nano <package_dir_name>/CMakeLists.txt

### add to CMakelist.txt
include_directories(include ${catkin_INCLUDE_DIRS})

add_executable(talker src/<package>.cpp)
target_link_libraries(<package> ${catkin_LIBRARIES})
add_dependencies(<package> <package_dir_name>_generate_messages_cpp)

### running new packages
    cd <ws_name>
    catkin_make
    source <ws_name>/devel/setup.zsh
    rosrun <package_dir_name> <package>
