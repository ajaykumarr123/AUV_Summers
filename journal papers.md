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
Based on the task, different modules are used for colour
and shape detection and coding is done using VB script.
The coding in VB Script provides the necessary control
signals to the thruster motors and other mechanisms for the
tasks to be performed. The control signals of the Roborealm
are given as inputs to Arduino mega with a pre-loaded
sketch to give the necessary PWM values to run the
thrusters.

###
