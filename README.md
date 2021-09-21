# QP-based MPC for Differential-Drive Mobile Robot Project
***
## ROS version : ROS melodic

## Required libraries
### Eigen Library : more than 3.0.0
### RBDL Library : more than 2.6.0

## Required Tools
### Google Cartographer for SLAM
### ROBOTIS TurtleBot3-burger
### Relaxed A star for global planner 
***
## Installation Guide

### RBDL
> RBDL requires ccmake to build successfully
- ccmake
```sh
sudo apt install cmake-curse-gui
```
- RBDL
```sh
git clone https://github.com/rbdl/rbdl
cd rbdl
mkdir build
cd build
ccmake ..
```
> Check the properties of ccmake below 
>> CMAKE_BUILD_TYPE=Release -DRBDL_BUILD_ADDON_URDFREADER=ON -DRBDL_USR_ROS_URDF_LIBRARY=OFF
```sh
make all
make install
```

### qpOASES
```sh
git clone https://github.com/coin-or/qpOASES.git
cd qpOASES
mkdir build
cd build
cmake ..
make all
make install
```