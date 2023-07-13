# ROS/ROS2 bridge for CARLA simulator

This is a fork of [carla-simulator/ros-bridge](https://github.com/carla-simulator/ros-bridge) to adapt ros humble and carla 0.9.14.

### Environment

* OS: ubuntu 22.04
* ROS2: Humble

### Installation

Install client library

* download [python package](https://github.com/gezp/carla_ros/releases/tag/0.9.14) for ubuntu22.04

```
 pip3 install <wheel-file-name>.whl
```

Build `carla-simulator/ros-bridge`
```bash
# cd workspace/src
git clone --recurse-submodules https://github.com/gezp/carla_ros.git
# install dependencies
cd ..
rosdep install --from-paths src --ignore-src -r
# complie
colcon colcon build --symlink-install
```

> Tip: carla server and client could run on differnet machines separately (or Docker Container), so you can install and run carla server on ubuntu18.04 which is officially supported platform, but run carla client and ROS on ubuntu22.04.
