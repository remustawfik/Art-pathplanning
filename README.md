##Setup
Instructions how to set up the visualization for pathfinding:
1. Follow http://wiki.ros.org/kinetic/Installation/Ubuntu to download ros kinetic (If you have not already)
2. Follow instructions here http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment 
Run the follwing in a terminal:
3. 'cd ~/catkin_ws/src'
4. 'catkin_create_pkg path_planning'
5. 'cd ~/catkin_ws'
6. 'catkin_make'
At this point, this should be how your file structure should look like:
Catkin_ws:
    build
    devel
    src:
    CMakeLists.txt
        Path_planning:
            CMakeLists.txt
            package.xml
7. 'cd path_planning'. Delete the CMakeLists.txt & package.xml. Copy all the files from github https://github.com/remustawfik/Art-pathplanning/tree/master/path_planning into your path_planning directory.
8. 'cd ~/catkin_ws'
9. ' catkin_make'
 **If this step fails, that usually means your path variables have not been initialized correctly, make sure you are using the same naming conventions as in the instructions**
 **SOMETIME catkin_make wont compile auto, you have to pass catkin_make --force-cmake**
10. 'cd ~/catkin_ws'
11. 'roscore'
12. In another terminal, 'source ~/catkin_ws/devel/setup.bash'
13. 'cd ~/catkin_ws/src/path_planning'
14. '$ for i in {1..5}; do rosrun path_planning path_planning ~/catkin_ws/src/path_planning/test/input/b_${i}.bmp ~/catkin_ws/src/path_planning/test/output/b_${i}.bmp; done'
15. Done. You should see the algorithm running and changing the output.bmp

