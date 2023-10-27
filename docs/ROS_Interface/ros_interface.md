# Creating the ROS node (Interface)

For each algorithm that the robot need to execute, should be created an ROS class node.

## Files

- template_cpp_ros_pkg
    - include
        - ros_cpp_template
            - template_ros_interface.hpp
            - template_ros_interface2.hpp
    - src
        - template_ros_interface.cpp
        - template_ros_interface2.cpp

## Programming Style

- Create a ROS node class.
- Define the subscriber and publisher. 
    - For each 'subscriber' the 'callback' will include a method that adapts the 'ros message' to the equivalent data neccesary to call the 'set' method from the algorithm class.
    - For each 'publsher' we recomend define a method 'send' that includes the 'publish' method and the previously data traduction from the 'get' method until 'ros message' adaptation.
- Define a 'run' method in order to include a 'while' with a 'spin'. In the 'while' should me contains the main program loop.
- The 'callback' functions should be private.
- The 'run' method must be public.
