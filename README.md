# Lab experiments for the course BITS F327 - AI for Robotics

- I hope you all have successfully installed ROS Kinetic on your system.
- All the experiment related files will be uploaded on this repository every week. 
- Clone (copy) this repo in your catkin_ws/src
- Always run `catkin_make` and `source./devel/setup.bash` after cloning new packages.

### Experiment 1
The first experiment is for you to learn about the basic ROS concepts like nodes, topics and messages.
- Install turtlebot3:
```
sudo apt-get update
sudo apt-get install ros-kinetic-turtlebot3*
```

- Run the following command to launch the simulation:
```
export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch
```

**Task**: Write a python script (publisher) that makes the robot move in a circle. (Hint: linear x=0.5, angular z=1.5, publish it on the topic "/cmd_vel"). Put the script in exp1/src folder.

Follow this: [ROS Documentation](http://wiki.ros.org/ROS/Tutorials/WritingPublisherSubscriber%28python%29)

- To view message type of /cmd_vel:
```
rostopic type /cmd_vel
```
You will get geometry_msgs/Twist which is the message type of the topic.
- To view the structure of the message:
```
rosmsg show geometry_msgs/Twist
```
The structure you get is how the data is stored in that topic. You will have to publish the data in that form to the topic /cmd_vel.


