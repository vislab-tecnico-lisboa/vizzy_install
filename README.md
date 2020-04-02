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
