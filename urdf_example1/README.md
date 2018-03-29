# Example 1
This package represents the simplest urdf description of a 4-wheeled robot that can also be used for simulation in Gazebo.

robot1 only uses the skid_steer driving plugin to drive the robot around in Gazebo.

robot2 also adds sensors with appropriate Gazebo plugins.

robot_state_publisher is used to publish the robot's tf tree from the parsed urdf file. However, in this simple implementation, Gazebo does not publish a topic containing the states of the non-fixed joints. Therefore, in RVIZ the view of the wheels isn't possible, because there is no tf for them. To overcome this problem, joint_state_publisher is used to always publish fake "0" state for these joints. This way, visualization in RVIZ is possible, albeit incorrect for the moving joints.
