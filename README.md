# vizzy_install
Scripts to install Vizzy repositories

## Ubuntu 16.04

Run the scripts in the vizzy-install repostory in the following order. You will be asked about the ROS version, which in this case is `kinetic`, and the location of your catkin workspace (e.g. `/home/user/my_catkin_ws`)

    cd  vizzy_install
    ./ros_install.sh
    source ~/.bashrc
    ./ros_packages_install.sh
    source ~/.bashrc
    ./install_yarp.sh
    source ~/.bashrc

## Ubuntu 18.04

Run the scripts in the vizzy-install repostory in the following order. You will be asked about the ROS version, which in this case is `melodic`, and the location of your catkin workspace (e.g. `/home/user/my_catkin_ws`)

    cd  vizzy_install
    ./ros_install.sh
    source ~/.bashrc
    ./ros_packages_install.sh
    source ~/.bashrc
    ./install_yarp_1804.sh
    source ~/.bashrc
 # Issues on 18.04
The script `ros_packages_install.sh` may fail because of mismatched versions of boost across several packages. To solve this issues:
* Remove `signals` from file `/usr/lib/x86_64-linux-gnu/cmake/gazebo/gazebo-config.cmake` at `command find_package(Boost`
* In the file [vizzy_tactile.cpp Line 131](https://github.com/vislab-tecnico-lisboa/vizzy_tactile_drivers/blob/master/vizzy_tactile/src/vizzy_tactile.cpp#L131), add `native_` to the variable `handler`
* Line 48 of the file `/usr/include/yaml-cpp/node/detail/iterator.h`, change `boost::next` to `std::next`
