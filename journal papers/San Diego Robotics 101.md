# [Cubeception 3]( https://robonation.org/sites/default/files/SDRobotics101_2016_RoboSub_Journal.pdf)

* Cubeception 3 uses quaternions to represent its orientation.</br> 
* An unscented Kalman filter is then used
to fuse the 9-Axis IMU data into an accurate estimation of the
robot’s orientation and velocity. </br>
* For depth estimation, Cubeception 3 uses its two pressure
sensors.</br>
* To facilitate communication between the different
subsystems, a distributed shared
memory system (DSM) was created.The DSM server and client software are written in C++, but
for convenience, a Python wrapper was also implemented.  </br>
* PID controllers are then utilized to
meet desired values for linear velocity and angular velocity.</br>
* A waypoint system based on dead reckoning was developed
to ease navigation to known locations.</br>
Forces and torques that act on the robot can be
estimated using knowledge of Cubeception 3’s geometry and
motor outputs</br>

## Computer Vision
Cubeception 3’s vision software utilizes two 5 megapixel
Raspberry Pi cameras connected to separate Raspberry Pi 2s
running OpenCV.</br>
Due to the water’s translucent nature, Cubeception 3 only
uses computer vision as a short range method to precisely
maneuver and attempt tasks. </br>

A forward-facing camera allows for detection of objects
directly in front of Cubeception 3.__The computer vision
algorithm on this camera begins by averaging all the pixels to
determine the hue of the background water in the image. This
dynamic color-determining algorithm allows for objects in the
frame to be isolated and categorized. They are put through a
shape recognition algorithm to determine whether they are
buoys, gates, or not of interest. From there, a contour-detection
algorithm and trigonometric calculations yield how far and in
which direction the objects are so Cubeception 3 can precisely
maneuver in an appropriate manner.__</br>

The second, downwards-facing camera has a separate
navigational algorithm. Cubeception 3 isolates the distinct
orange color of the tape lining the bottom of the pool. It also
uses its depth sensors to estimate the expected difference
between the color of the tape compared to the floor of the pool.
Cubeception 3 does this because the lighting varies at different
depths and a static tape recognition routine may not properly
detect the tape in certain situations.
