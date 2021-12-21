# indy7_moveit2_config
This package contains Indy7 configuration files (yaml, srdf) to use MoveIt2 package in ROS2 environment.

# Install & Build
The following commands download a package from a remote repository and install it in your colcon workspace.

```bash
mkdir -p ~/robot_ws/src # Make colcon workespace directory. If colcon workspace does not exist, run this command.
cd ~/robot_ws/src
git clone https://github.com/HYU-PBLRC-PB1/indy7_moveit2_config.git # Download the package from the remote repository.
cd ~/robot_ws && colcon build --symlink-install # Build colcon workspace.
```

# Package Structure
If you want to check the file structure of a package, run the following command.
```bash
cd ~/robot_ws/src/indy7_moveit2_config
tree
```

```bash
indy7_moveit2_config
├── CMakeLists.txt
├── config
│   ├── fake_control
│   │   ├── controllers.yaml
│   │   ├── indy7_arm_controller.yaml
│   │   └── start_position.yaml
│   ├── joint_limits.yaml # Joint acceleration and velocity limits
│   ├── kinematics.yaml # Kinematic analysis, library designation
│   └── ompl_planning.yaml # Inverse kinematics for move_group, planner
├── launch
│   ├── move_group_action_server.launch.py
│   ├── move_group_fake_control.launch.py
│   ├── rviz_interactive.rviz
│   └── rviz.rviz
├── LICENSE
├── package.xml
├── README.md
└── srdf
    ├── indy7_arm.srdf.xacro # srdf file with simple reference to indy7_arm.xacro 
    ├── indy7_arm.xacro #This file contains information about indy7's base, end-effector, link, joint, ignoring collisions, etc.
    └── indy7.srdf 
```
