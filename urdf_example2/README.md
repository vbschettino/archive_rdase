# Example 2
In this second implementation there's support for low level control of each of the joints in Gazebo (PID controllers for velocity or effort, for example).

This way, only one controller plugin is loaded in Gazebo, and the custom controllers are defined from parameters loaded in the ros parameter server. This approach also gives natural support for a joint_state publisher, without the need for a specific plugin.

This approach gives more control over the simulation, enabling it to be more realistic, but also adds more complexity.