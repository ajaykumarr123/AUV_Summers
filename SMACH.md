# SMACH
SMACH is a task-level architecture for rapidly creating complex robot behavior. At its core, SMACH is a ROS-independent Python library to build hierarchical state machines. SMACH is a new library that takes advantage of very old concepts in order to quickly create robust robot behavior with maintainable and modular code.
Smach, which stands for "State Machine", is a powerful and scalable Python-based library for hierarchical state machines. The Smach library does not depend on ROS, and can be used in any Python project. The executive_smach stack however provides very nice integration with ROS, including smooth actionlib integration and a powerful Smach viewer to visualize and introspect state machines.
### Creating a state
To create a state, you simply inherit from the State base class, and implement the State.execute(userdata) method:


```
  class Foo(smach.State):
     def __init__(self, outcomes=['outcome1', 'outcome2']):
       # Your state initialization goes here

     def execute(self, userdata):
        # Your state execution goes here
        if xxxx:
            return 'outcome1'
        else:
            return 'outcome2'
 ```
In the init method you initialize your state class. Make sure to never block in the init method! If you need to wait for other parts of your system to start up, do this from a separate thread.

In the execute method of a state the actual work is done. Here you can execute any code you want. It is okay to block in this method as long as you like. Once you return from this method, the current state is finished.

When a state finishes, it returns an outcome. Each state has a number of possible outcomes associated with it. An outcome is a user-defined string that describes how a state finishes. A set of possible outcomes could for example be ['succeeded', 'failed', 'awesome']. The transition to the next state will be specified based on the outcome of the previous state.

### Adding states to a state machine
A state machine is a container that holds a number of states. When adding a state to a state machine container, you specify the transitions between the states.

```
  sm = smach.StateMachine(outcomes=['outcome4','outcome5'])
  with sm:
     smach.StateMachine.add('FOO', Foo(),
                            transitions={'outcome1':'BAR',
                                         'outcome2':'outcome4'})
     smach.StateMachine.add('BAR', Bar(),
                            transitions={'outcome2':'FOO'})
The resulting state machine looks like this:
```
