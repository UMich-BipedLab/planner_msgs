cmake_minimum_required(VERSION 2.8.3)
project(planner_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

find_package(
    catkin REQUIRED COMPONENTS
    message_generation
    geometry_msgs
)

add_message_files(
    FILES
    FootPlacementArray.msg
    FootPlacement.msg
    State.msg
    Terrain.msg
    Plane.msg
    PlaneArray.msg
    Torso.msg
    WaypointArray.msg
    Waypoint.msg
)

generate_messages(
    DEPENDENCIES std_msgs geometry_msgs
)

catkin_package(
    CATKIN_DEPENDS message_runtime
)
