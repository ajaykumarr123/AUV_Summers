# journal papers

### SRM University

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



### Team BangaloreRobotics

The software used in LASSIE IV starts from image
processing tool RoboRealm, different modules in this
software tool perform the image recognition and also
provides the Centre of Gravity of the image being
processed. </br>
Based on the task, different modules are used for colour and shape detection and coding is done using VB script.The coding in VB Script provides the necessary control signals to the thruster motors and other mechanisms for the tasks to be performed. The control signals of the Roborealm are given as inputs to Arduino mega with a pre-loaded sketch to give the necessary PWM values to run the thrusters.

### San Diego City College

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
Figure 2: Early Software Development flowchart.
Hal9000 program now part of Heimdall vision recognition
program.  </br>
Due to these issues, several communication
methods were explored, with the final design
utilizing I2C communication. This adjustment
allowed the Jetson TK-1 board to convey variables to
the PID system in large messages in under a
millisecond, improving vehicle response to near real
time. This configuration utilizes an event-based
system for determining vehicle motion, with
reactions occurring in response to recognized
competition course obstacles. Objects are identified
and determined in relation to the vehicle via the
Heimdall Open CV system. This data is then paired
with information received from the MPU 6050 IMU
to determine the Scarborough's location in relation to
it's selected tasks, and actions necessary to complete
the chosen competition challenges. These
advancements provide a significant development
upon last year's dependencies on hard values,
allowing the team to further develop the vehicle's
positioning systems in years to come.
