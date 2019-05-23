# journal papers

### SRM University

The Software stack of Sedna is built on top
of the Robot Operating System (ROS) by
Willow Garage. ROS is installed on top of
Debian Linux operating system, running
on an Intel core i7 processor. A Mini-ITX
on-board computer is provided inside the
pressure hull.
The software stack has been designed from
scratch this year and provides the
following benefits:
 Modular design with optimal task
distribution
 Abstract asynchronous inter-process
communication mechanisms
 Redundancy in process life-cycles in
case of crashes
 Shared memory system for vehicle
parameter variables
 Improved front-end controls for easy
debugging of missions
The Robot Operating System is an
industrial-grade robotics framework which
provides various services and tools that
significantly reduce design cycle time. The
software stack of Sedna is modularized
into various processes that are completely
independent of each other, yet are able to
communicate using an asynchronous
messaging protocol.
The software subsystems of Sedna are
divided as such:
 Mission Planner
 Motor Controller
 Vision Server
 Action Server/ Action Client
 User Front End
 Telemetry
All these systems are integrated into the
ROS infrastructure in the form of nodes
with asynchronous communication among
them. Topics provide data communication
over TCP or UDP and Services provide an
XML-RPC request-response call. The 
