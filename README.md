# DroneControlDNN
This repository contains a ROS package which include several nodes to 
control the drone.  
The main goal of this package is to allow the drone to avoid the object 
automatically.
The main node are:
- camera node
- recognition node
- control node

### camera node
Basically, this node just grab the frame for the onboard camera and 
publish it as topic.

### recognition node
This node subscribes to the camera node, load the recognition 
model, process the frame and send the result as topic.

### control node
This node subscribes to the recognition node and regarding the result of
the regognition, it will send different messages to the MAVROS node in 
order to send data to the flight controller.

## Table of contents

1. [Installation](#installation)
2. [Utilisation](#utilisation)
3. [Contributin](#contributing)
4. [Licence](#licence)

## Installation
To install this package, just clone the repository in your workspace and
rebuilt it.
Also modify the ros.yalm to fit your requirements (camera name, topic name, etc).

### Dependencies
This package depends on several ROS dependencies.
- cv_bridge
- rospy
- roscpp
- MAVROS
- tensorflow
- keras
- TensorRT

## Utilisation
To run this node, just use the following command:  
- `roslaunch droneControlDNN together.launch`

## Contributing

* **Schoninger Jimmy** <schoninger@enroute.co.jp>

## Licence
This project is under the EnRoute copyright.
