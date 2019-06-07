#  [ReDefiance](https://robonation.org/sites/default/files/SDStateUni_2016_RoboSub_Journal.pdf) 

* The software system uses an ASUS mini-ITX
motherboard equipped with an Intel i7-4790k Quad-Core
Processor, 8GB of Memory, and a 256GB SSD.</br>
* customizable
graphical user interface (GUI), was programmed and
implemented.The GUI displays gauges of the
vehicle’s status which includes its yaw, pitch, and roll,
depth, position and velocity, voltage and current levels,
duty cycle percentages of the motors, alerts/warnings,
and internal temperature for detecting leaks. </br>
* Image processing throughout the obstacle course is
accomplished with the GUI using OpenCV and 
Python.Utilizing OpenCV with
Python, the team was able to develop our own algorithms
for detecting objects that contain a specific Hue,
Saturation and Value (HSV), as well as a certain number
of contours. </br>

* In addition, segmentation and shape detection were added
to make the algorithms more robust. Given a situation
where the vehicle needed to respond based on the shape
present in an image it is tracking, it is able to compare
the number of angles found between a contour to do so.
This is done by *segmenting* the image, removing the
background and other objects outside of the region of
interest. The software looks for the number of angles to
determine the shape detected on this segmented image
for higher fidelity results.
