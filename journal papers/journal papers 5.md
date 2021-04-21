
### SRM University([Sedna 2.0](https://robonation.org/sites/default/files/SRMUni_2016_RoboSub_Journal.pdf) )

The Software stack of Sedna is built on top  of the Robot Operating System (ROS) by Willow Garage. **A Mini-ITX on-board computer is provided inside the pressure hull.**  </br>
The software stack provides the following benefits:  </br>
 Abstract asynchronous inter-process
communication mechanisms </br>
 Redundancy in process life-cycles in
case of crashes  </br>
 Shared memory system for vehicle
parameter variables  </br>
 The software stack of Sedna is modularize into various processes that are completely independent of each other, yet are able to communicate using an **asynchronous messaging protocol.**  </br>
The software subsystems of Sedna are divided as such:
 Mission Planner
 Motor Controller
 Vision Server
 Action Server/ Action Client
 User Front End
 Telemetry  </br>
All these systems are integrated into the ROS infrastructure in the form of nodes with asynchronous communication among them.**Topics provide data communication over TCP or UDP and Services provide an XML-RPC request-response call.** The software team is mainly responsible for developing software for mission planning, computer vision and active vehicle localization. 



### Team BangaloreRobotics([Lassie IV](https://robonation.org/sites/default/files/TeamBangaloreRobotics_2016_RoboSub_Journal.pdf) )

The software used in LASSIE IV starts from image
processing tool RoboRealm, different modules in this
software tool perform the image recognition and also
provides the Centre of Gravity of the image being
processed. </br>
Based on the task, different modules are used for colour and shape detection and coding is done using VB script.The coding in VB Script provides the necessary control signals to the thruster motors and other mechanisms for the tasks to be performed. The control signals of the Roborealm are given as inputs to Arduino mega with a pre-loaded sketch to give the necessary PWM values to run the thrusters.

### San Diego City College([Scarborough](https://robonation.org/sites/default/files/SDCityColl_2016_RoboSub_Journal.pdf) )

During the first major iteration of software development, serial communication devices were
used as the vehicle's primary data sharing method. A
*PID system* was programmed onto an Arduino Mega
to dynamically control the Vehicle's motor speeds to
match desired direction and endpoint. The Jetson
TK-1 board was utilized to determine via sensor
measurements the vehicle's yaw, pitch roll, and
depth, which were passed onto the microcontroller to
determine the thruster motor values. Response times
with this method were slow however, due to
excessive data flow through the microcontroller and
compounded serial communication times.
  </br>
Due to these issues, several communication
methods were explored, with the final design
utilizing *I2C communication*. This adjustment
allowed the Jetson TK-1 board to convey variables to
the PID system in large messages in under a
millisecond, improving vehicle response to near real
time. This configuration utilizes an event-based
system for determining vehicle motion, with
reactions occurring in response to recognized
competition course obstacles. 

### Oregon Institute of Technology, OTUS/AUVSI Club ([OTUS](https://robonation.org/sites/default/files/OregonTech_2016_RoboSub_Journal%20%281%29.pdf) )

MicroStrain Lord 3DM-GX4-45 is an Aperture Heading
Reference System (AHRS) sensor and used to measure speed
and angle of the OTUS vehicle for navigation, measuring the
attitude such as position and linear velocity from three-axis
accelerometers and angle and angular velocity from three-axis
gyros. We don’t use magnetometers and GPS in underwater
circumstances. But we are additionally utilizing a pressure
sensor (BAR30-SEMSPR-R1) for measuring depth in 2mm
resolution because of possible drift from inside the pressure
altimeter sensor.
hydrophones have to find correct direction and signal. </br>
Incorporated into above INS sensor, BlueRobotics’s BAR30-
R1 absolute pressure/altitude sensor (0-30 bar barometer) is
used to measure the depth with 2mm depth resolution. The
compact sensor is easily converted to the depth (altitude) and
really inexpensive sensor and is connected with Arduino
Mega via I2C communication. This sensor will be
incorporated into altimeter sensor in the INS sensor.


### Prairie View A&M University([Panther](https://robonation.org/sites/default/files/PrairieViewUni_2016_RoboSub_Journal.pdf) )
The computer system interfaces using USB connectors with the
motor controllers, the NI MyRio, and the Logitech C920
webcams.
By using LabVIEW, you can build on top of tested, supported, and maintained libraries of lower level code
from NI. Choosing C means you’ll need to implement, support, and maintain your own lower level libraries or
purchase them from a vendor.  </br>
Syntax-wise, C is optimized for sequential execution of
instructions as fast as the CPU can handle them. This is
perfect for pure computation, when only one task is being
executed and instructions are more basic. *The graphical syntax
in LabVIEW*, on the other hand, is optimized for the parallel
execution of tasks that have real-world timing constraints
The current Sub already have LabVIEW implement.


