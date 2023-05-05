# depth-camera-ros-gazebo
Depth camera simulation (Kinect) for test your vision algorithms on Gazebo/ROS 1.

Some notes about it:

- Place unzipped folder under "~/.gazebo/models".
- You'll be using the generic "Openni Kinect" plugin. You can (and should) use this plugin for other types of depth cameras besides the Kinect (it's an older plugin, and so it retains its old name).
- Open Gazebo with ROS support enabled (e.g. roslaunch gazebo_ros empty_world.launch). Use the Insert panel to find your "Kinect ROS" model, and insert it into the world. You must source your ROS environment before use "roslaunch".
- By default, the camera is set to static for testing purpose (in model.sdf).
- Ensure that your RViz Fixed Frame matches the frameName you specified in the <plugin> tag.
- Add pointcloud2 item to RVIZ, subscribe to "/camera/depth/points".
