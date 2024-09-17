# Navvis Description Package

## Overview

This package is used to describe the robot model in URDF and visualize it in RViz. It follows the ROS package structure and contains necessary files for configuring and launching the robot model. 

## Package Structure

```arduino
navvis_description/
│
├── CMakeLists.txt
├── package.xml
├── README.md
├── launch/
│   └── display.launch
│
├── config/
│   └── config.rviz
│
└── urdf/
    ├── robot.urdf
    └── robot.xacro
```

### 1. Launch Files

The launch file `display.launch` is provided to start the robot description in RViz. It accepts the following three arguments:
- `use_xacro`: A boolean flag that determines if xacro files should be used to parse the robot description.
- `file`: The file path to the robot description (URDF or XACRO).
- `use_joint_state_publisher_gui`: A flag to enable or disable the `joint_state_publisher` GUI.

### 2. Configuration Files

The RViz configuration file `config.rviz` is included to define how the robot model should be displayed in RViz.

### 3. URDF Files

The URDF directory contains:
- `robot.urdf`: A URDF description of the robot model.
- `robot.xacro`: A XACRO-based robot description file for dynamic robot model generation.

## Usage

To visualize the robot model in RViz, you can use the `display.launch` file by running the following command:

```bash
roslaunch navvis_description display.launch use_xacro:=true file:=urdf/robot.xacro use_joint_state_publisher_gui:=true
```

Make sure to modify the arguments (`use_xacro`, `file`, `use_joint_state_publisher_gui`) according to your specific needs.

## License

This project is licensed under the [MIT License](LICENSE).

