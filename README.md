# Skibot

A turtlesim style ROS simulator with simple physics.

see instead: <https://github.com/JMU-ROBOTICS-VIVA/skibot>

## Nodes

### skibot_node

#### Subscribed Topics
* `thrust` (`geometry_msgs/Wrench`) 

	Force applied to the Skibot. The skibot will execute the command
	for .6 seconds before timing out. Only `force.x` and `torque.z`
	are used. All other fields will be ignored. Linear force is
	clipped to (-5.0, 5.0) and torque is clipped to (-.2, .2).
	
*  `target_pose`  (`skibot/Pose`)

	The pose will be drawn to the screen as a green arrow.  May be used to
	visualize a goal pose.
   
*  `target_point`  (`geometry_msgs/Point`)

   	The point will be drawn to the screen as a green circle.  May be used to
	visualize a goal point.

#### Published Topics

* `pose`  (`skibot/Pose`)

	Current robot pose.
	
#### Services 

* `teleport` (`skibot/Teleport`)

	Teleport to the indicated location and set velocity to zero.
