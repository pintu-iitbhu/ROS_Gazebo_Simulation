# ROS_Gazebo_Simulation
[ROS](http://wiki.ros.org/ROS/Tutorials) (Robot Operating System) can be used with [PX4](https://github.com/pkyadav73199/Firmware) and the [Gazebo simulator](https://dev.px4.io/v1.9.0/en/simulation/gazebo.html). It uses the MAVROS MAVLink node to communicate with PX4.

### Before coming to ROS with Gaszebo Simulation you need prior setting.You can find here [Autonomous_Quadcopter](https://github.com/pkyadav73199/Autonomous_Quadcopter)

## PX4 installation
```
mkdir -p ~/src
cd ~/src
git clone https://github.com/pkyadav73199/Firmware.git
cd Firmware
git submodule update --init --recursive
```
