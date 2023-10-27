# Package Name 
#### (:construction: Working :construction:)

## Overview

This is a template: replace, remove, and add where required. Describe here what this package does and what it's meant for in a few sentences.

**Keywords:** example, package, template

Or, add some keywords to the Bitbucket or GitHub repository.

### License

TO DO
<!-- The source code is released under a [BSD 3-Clause license](ros_package_template/LICENSE). -->

**Author: Dahui Lin<br />
Affiliation: [Robotics and Mechatronics Group (University of Málaga)](https://www.uma.es/robotics-and-mechatronics/)<br />
Maintainer: Dahui Lin Yang, dahuilinyang@uma.com**

<!-- This is research code, expect that it changes often and any fitness for a particular purpose is disclaimed. -->

<!-- [![Build Status](http://rsl-ci.ethz.ch/buildStatus/icon?job=ros_best_practices)](http://rsl-ci.ethz.ch/job/ros_best_practices/) -->

![Example image](doc/example.jpg)


### Publications

If you use this work in an academic context, please cite the following publication(s):

* Francisco Pastor, Da-hui Lin-Yang, Jesús M Gómez-de-Gabriel, Alfonso J García-Cerezo: **PAPER TITLE**. Dataset with Tactile and Kinesthetic Information from a Human Forearm and Its Application to Deep Learning. ([PDF](https://doi.org/10.3390/s22228752))

			@article{pastor2022dataset,
			title={Dataset with Tactile and Kinesthetic Information from a Human Forearm and Its Application to Deep Learning},
			author={Pastor, Francisco and Lin-Yang, Da-hui and G{\'o}mez-de-Gabriel, Jes{\'u}s M and Garc{\'\i}a-Cerezo, Alfonso J},
			journal={Sensors},
			volume={22},
			number={22},
			pages={8752},
			year={2022},
			publisher={MDPI}
        }


## Installation

### Installation from Packages
    
Use `rosdep`:

	sudo rosdep install --from-paths src

### Building from Source

#### Building

To build from source, clone the latest version from this repository into your catkin workspace and compile the package using

	cd catkin_workspace/src
	git clone https://github.com/ethz-asl/ros_best_practices.git
	cd ../
	rosdep install --from-paths . --ignore-src
	catkin_make

## Usage

Describe the quickest way to run this software, for example:

Run the main node with

	roslaunch ros_package_template ros_package_template.launch

## Config files

Config file folder/set 1

* **config_file_1.yaml** Shortly explain the content of this config file

Config file folder/set 2

* **...**

## Launch files

* **launch_file_1.launch:** shortly explain what is launched (e.g standard simulation, simulation with gdb,...)

     Argument set 1

     - **`argument_1`** Short description (e.g. as commented in launch file). Default: `default_value`.

    Argument set 2

    - **`...`**

* **...**

## Nodes

### ros_package_template

Brief description of the pakage.


#### Subscribed Topics

* **`/temperature`** ([sensor_msgs/Temperature])

	The temperature measurements from which the average is computed.


#### Published Topics

...


#### Services

* **`get_average`** ([std_srvs/Trigger])

...


### NODE_B_NAME

...


## Bugs & Feature Requests

