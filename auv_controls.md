# AUV_CONTROLS

### Code
```c++

#include <ros/ros.h>
#include <kraken_msgs/thrusterData6Thruster.h>
#include <geometry_msgs/Pose.h>
#include <iostream>
#include <algorithm>
using namespace std;

ros::Publisher pub;
const float PI = 3.14159265;
float rate = 10;
geometry_msgs::Pose current_pose;

kraken_msgs::thrusterData6Thruster getMessage(double linear_x)
{
    kraken_msgs::thrusterData6Thruster msg;
    msg.data[2] = linear_x;
    msg.data[3]=linear_x;
    msg.data[0] =0;
    msg.data[1] =0;
    msg.data[4] =0;
    msg.data[5] = 0;
    return msg;
}

void poseCallback(const geometry_msgs::Pose::ConstPtr& msga)
{
    current_pose = *msga;
}

int main(int argc, char** argv)
{
    ros::init(argc, argv, "mykraken_control");
    ros::NodeHandle h;
    pub = h.advertise<kraken_msgs::thrusterData6Thruster>("kraken/control/thruster6pid", 1000);
    ros::Subscriber sub = h.subscribe("/KrakenSimulator/Pose", 1000, poseCallback);
    ros::Rate loopRate(rate);

    double x0;
    const double tolerance = 0.25;

    while (ros::ok())
    {
        cout << "Enter target: ";
        cin >> x0 ;

        while (ros::ok()) {
            loopRate.sleep();
            ros::spinOnce();
            cout << current_pose.position.x << endl;

             double distance = abs(x0-current_pose.position.x);
            if (distance < tolerance) {
                pub.publish(getMessage(0));
                break;
            }
 
 
            kraken_msgs::thrusterData6Thruster msg = getMessage(min(100*distance, 120) );

            pub.publish(msg);
        }
    }
    return 0;
}
```
