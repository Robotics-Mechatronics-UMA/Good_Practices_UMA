# Creating the Aglorithms

The next codefiles are the templates for coding the algorithms. Also, extra .hpp and .cpp files can be added if you want to create differents algorithms or libraries.

**They do not contain ROS libraries** :bagbang:

## Files

- template_cpp_ros_pkg
    - include
        - ros_cpp_template
            - template_library.hpp
            - template_library2.hpp
    - src
        - template_library.cpp
        - template_library2.cpp


## Programming Style

- Use class programming.
- If it is not defined, create your struct variable to represent the robot state.
- It is recommended to implement class type methods Set()'s and Get()'s for each variable which you want to get or to change the value.
- The variables from the class should be private.
- The methods that only is used by the class should be private.
- The methods Set()'s, Get()'s must be public.
- The methods which will be used for ROS node interface or other algorithms must be public.
- Usually the .hpp file contains the definition of the class and .cpp the implementation of the methods.

