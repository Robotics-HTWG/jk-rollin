# Description Package for JK_Rollin Robot
This packages contains the description of the JK_Rollin robot in the xacro format. The ROS build in tools are used to convert it to urdf models for visualization in RViz or for simulation in Gazebo. The package also contains a launch file to visualize the robot in RViz

## Install 
Install the required dependencies using the rosdep install command from your workspace folder e.g. ros2_ws
```
rosdep install --from-paths src -y --ignore-src 
```

Due to some bugs in the ROS2 Humble rosdeps, you have to install the following packages manually
```
sudo apt install ros-humble-joint-state-publisher-gui ros-humble-xacro
```

## Build
To build the jk_rollin_description package run in your workspace directory e.g. ros2_ws
```
colcon build --symlink-install --packages-select jk_rollin_description 
```

## RViz Visulaization
To display the JK_Rollin robot in RViz launch
```
ros2 launch jk_rollin_description display.launch.py
```