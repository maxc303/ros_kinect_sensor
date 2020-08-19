# ros_kinect_sensor

The repo is for xbox 360 kinect sensor being used in ROS.

Kinect Setup:

1. Install freenect
<pre>
git clone https://github.com/OpenKinect/libfreenect.git    
cd libfreenect    
mkdir build   
cd build    
cmake -L ..    
make
sudo make install
</pre>

2.Create a catkin workspace and make the freenect_stack, rgbd_launch is found to be required.
<pre>
mkdir catkin_ws
cd catkin_ws
mkdir src
cd src 
catkin_init_workspace
#
git clone https://github.com/ros-drivers/freenect_stack.git
git clone https://github.com/ros-drivers/rgbd_launch.git
cd ..
catkin_make

</pre>

3.Test the sensor
http://wiki.ros.org/freenect_launch
http://wiki.ros.org/rgbd_launch
<pre>
#under catkin_ws, source the workspace file
. devel/setup.bash
roslaunch freenect_launch freenect.launch
#Use Rviz or rqt to visualize the images or pointcloud

</pre>
