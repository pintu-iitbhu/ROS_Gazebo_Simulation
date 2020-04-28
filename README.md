# ROS_Gazebo_Simulation
[ROS](http://wiki.ros.org/ROS/Tutorials) (Robot Operating System) can be used with [PX4](https://github.com/pkyadav73199/Firmware) and the [Gazebo simulator](https://dev.px4.io/v1.9.0/en/simulation/gazebo.html). It uses the MAVROS MAVLink node to communicate with PX4.

### Before coming to ROS with Gaszebo Simulation you need prior setting.You can find here [Autonomous_Quadcopter](https://github.com/pkyadav73199/Autonomous_Quadcopter)

## Installation
Gazebo 7 setup is included in our standard build instructions.
* Linux: Development Environment on Linux (Ubuntu 16.04) > jMAVSim/Gazebo Simulation

To install the Gazebo9 and jMAVSim simulators:
1. Download [ubuntu_sim.sh].
2. Run the script in a bash shell:
```
source ubuntu_sim.sh
```
To install the development toolchain:
1. Download [ubuntu_sim_ros_gazebo.sh](https://github.com/pkyadav73199/ROS_Gazebo_Simulation/blob/master/ubuntu_sim_ros_gazebo.sh).
2. Run the script in a bash shell:
```
source ubuntu_sim_ros_gazebo.sh
```

## PX4 installation
```
mkdir -p ~/src
cd ~/src
git clone https://github.com/pkyadav73199/Firmware.git
cd Firmware
git submodule update --init --recursive
```

## Running UAV Simulation with px4 firmware
```
cd ~/src/Firmware
make px4_sitl gazebo
```
# Putting it all together 
1. Start ROS master as mentioned above
2. Start gazebo 
```markdown
cd ~/src/Firmware
make px4_sitl gazebo
```
3. Launch px4 with mavros
```markdown
roslaunch mavros px4.launch fcu_url:="udp://:14540@127.0.0.1:14540"
```
4. Running ros node for created task
```markdown
cd ~/catkin_ws
source ./devel/setup.bash 
rosrun offb uav
```
